Subject: [[Google Cloud Platform]] #gcp  

-------------------1

gcloud container clusters create onlineboutique-cluster-826 --zone europe-west4-a --machine-type e2-standard-2 --num-nodes 2 --release-channel rapid


kubectl create namespace dev && \
kubectl create namespace prod


kubectl config set-context --current --namespace=dev


-------------------2

gcloud container node-pools create optimized-pool-6378 \
  --cluster=onlineboutique-cluster-826 \
  --machine-type=custom-2-3584 \
  --num-nodes=2 \
  --zone=europe-west4-a
  
for node in $(kubectl get nodes -l cloud.google.com/gke-nodepool=default-pool -o=name); do
  kubectl cordon "$node";
done

for node in $(kubectl get nodes -l cloud.google.com/gke-nodepool=default-pool -o=name); do
  kubectl drain --force --ignore-daemonsets --delete-local-data --grace-period=10 "$node";
done


gcloud container node-pools delete default-pool --cluster onlineboutique-cluster-826 --zone europe-west4-a


-------------------3

kubectl create poddisruptionbudget onlineboutique-frontend-pdb --selector run=frontend --min-available 1


-------------------4

kubectl autoscale deployment frontend --cpu-percent=50 --min=1 --max=13


gcloud beta container clusters update onlineboutique-cluster-826 --enable-autoscaling --min-nodes 1 --max-nodes 6