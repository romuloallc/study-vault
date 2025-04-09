Subject: [[Google Cloud Platform]] #gcp  

```
gcloud container clusters create echo-cluster --zone us-central1-b --machine-type e2-standard-2 --num-nodes 2
```

```
gcloud auth configure-docker
```

```
docker tag hello-world:latest gcr.io/**PROJECT_ID**/hello-world:v1
```

```
docker push gcr.io/**PROJECT_ID**/hello-world:v1
```

```
docker pull gcr.io/**PROJECT_ID**/hello-world:v1
```

```
gcloud container images list-tags gcr.io/**PROJECT_ID**/hello-world
```

```
gcloud container images describe gcr.io/**PROJECT_ID**/hello-world:**VERSION**
```