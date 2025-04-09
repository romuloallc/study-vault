Subject: [[Google Cloud Platform]] #gcp  

Trocar de projeto
```bash
gcloud config set project [id-do-projeto]
```

IAP tunnel
```bash
gcloud compute start-iap-tunnel [instance-name] 3389 --local-host-port=localhost:3389 --zone=southamerica-east1-a
```

```bash
gcloud compute start-iap-tunnel [instance-name] 3389 --local-host-port=localhost:3389 --zone=us-central1-a
```

```[bash]
gcloud compute forwarding-rules list
gcloud compute addresses list --filter=EXTERNAL

# Filtrado

gcloud compute addresses list --filter=EXTERNAL | awk '{print $1, $2, $3}'
gcloud compute forwarding-rules list | awk '{print $1, $3}'
```