# practicehabits

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
