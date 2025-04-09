###### Creating VPC
```[bash]
gcloud compute networks create vpc-lab --project=labs-456119 --subnet-mode=custom --mtu=1460 --bgp-routing-mode=regional --bgp-best-path-selection-mode=legacy
```
###### Creating Subnet
```[bash]
gcloud compute networks subnets create subnet-lab --project=labs-456119 --range=10.0.0.0/29 --stack-type=IPV4_ONLY --network=vpc-lab --region=us-central1 --enable-private-ip-google-access
```
###### Creating Firewall Rule
```[bash]
gcloud compute firewall-rules create vpc-lab-allow-custom --project=labs-456119 --network=projects/labs-456119/global/networks/vpc-lab --description=Allows\ connection\ from\ any\ source\ to\ any\ instance\ on\ the\ network\ using\ custom\ protocols. --direction=INGRESS --priority=65534 --source-ranges=10.0.0.0/29 --action=ALLOW --rules=all
```
##### Creating IAP Rule
```[bash]
gcloud compute --project=labs-456119 firewall-rules create allow-iap --direction=INGRESS --priority=1000 --network=vpc-lab --action=ALLOW --rules=tcp:22 --source-ranges=35.235.240.0/20
```
##### Creating IAP Rule
```[bash]
gcloud compute instances create instance-lab \

--project=labs-456119 \

--zone=us-central1-c \

--machine-type=e2-micro \

--network-interface=network-tier=PREMIUM,stack-type=IPV4_ONLY,subnet=subnet-lab \

--metadata=enable-osconfig=TRUE \

--maintenance-policy=MIGRATE \

--provisioning-model=STANDARD \

--service-account=221800070453-compute@developer.gserviceaccount.com \

--scopes=https://www.googleapis.com/auth/devstorage.read_only,https://www.googleapis.com/auth/logging.write,https://www.googleapis.com/auth/monitoring.write,https://www.googleapis.com/auth/service.management.readonly,https://www.googleapis.com/auth/servicecontrol,https://www.googleapis.com/auth/trace.append \

--create-disk=auto-delete=yes,boot=yes,device-name=instance-lab,image=projects/ubuntu-os-cloud/global/images/ubuntu-2204-jammy-v20250312,mode=rw,size=10,type=pd-standard \

--create-disk=auto-delete=yes,device-name=disk-lab,mode=rw,name=disk-lab,size=10,type=pd-balanced \

--no-shielded-secure-boot \

--shielded-vtpm \

--shielded-integrity-monitoring \

--labels=goog-ops-agent-policy=v2-x86-template-1-4-0,goog-ec-src=vm_add-gcloud \

--reservation-affinity=any \

&& \

printf 'agentsRule:\n packageState: installed\n version: latest\ninstanceFilter:\n inclusionLabels:\n - labels:\n goog-ops-agent-policy: v2-x86-template-1-4-0\n' > config.yaml \

&& \

gcloud compute instances ops-agents policies create goog-ops-agent-v2-x86-template-1-4-0-us-central1-c \

--project=labs-456119 \

--zone=us-central1-c \

--file=config.yaml
```


