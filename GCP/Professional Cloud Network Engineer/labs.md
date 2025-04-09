Subject: [[Google Cloud Platform]] #gcp  

```[bash]
gcloud compute networks create managementnet --project=qwiklabs-gcp-04-65dd68eb168d --subnet-mode=custom --mtu=1460 --bgp-routing-mode=regional && 

gcloud compute networks subnets create managementsubnet-us --project=qwiklabs-gcp-04-65dd68eb168d --range=10.130.0.0/20 --stack-type=IPV4_ONLY --network=managementnet --region=us-east4
```

```[bash]
gcloud compute --project=qwiklabs-gcp-04-65dd68eb168d firewall-rules create managementnet-allow-icmp-ssh-rdp --direction=INGRESS --priority=1000 --network=managementnet --action=ALLOW --rules=tcp:22,tcp:3389,icmp --source-ranges=0.0.0.0/0
```


https://cloud.google.com/blog/products/networking/perfkit-benchmarker-for-evaluating-cloud-network-performance

