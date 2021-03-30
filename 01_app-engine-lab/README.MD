# Deploying an App Engine Application
```Cloud shell make bucket regional storage class
gsutil mb -c regional -l us-east1 gs://pkammas-bucket
```

```make it publicly vieweable
gsutil iam ch allUsers:objectViewer gs://pkammas-bucket
```

git clone https://github.com/linuxacademy/content-gc-essentials
cd content-gc-essentials/app-engine-lab

gcloud config set app/cloud_build_timeout 6000s
gcloud app deploy

gcloud app browse