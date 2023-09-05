# Host a static website on GCP Storage Bucket

[www.practicehabits.net](https://www.practicehabits.net)

## History
- 20230905: move from gcp storage bucket to firebase hosting


```bash

gcloud auth login

gcloud config list

gcloud config set account `ACCOUNT`

gcloud projects list

```

Create bucket:  
```bash
export BUCKET_NAME="www.practicehabits.net"
gsutil mb -l us-east1 gs://$BUCKET_NAME
gsutil iam ch allUsers:objectViewer gs://$BUCKET_NAME
```

Copy website content
```bash
# cd to root directory of website content
gsutil rsync -R . gs://$BUCKET_NAME

```
