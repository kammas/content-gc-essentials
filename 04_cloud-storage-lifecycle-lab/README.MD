# Setting Cloud Storage Lifecycle Rules

```
# make bucket
gsutil mb -c regional -l us-east1 gs://pkammas-bucket1

#check lifecycle rules of bucket
gsutil lifecycle get gs://pkammas-bucket1

git clone https://github.com/kammas/content-gc-essentials
cd content-gc-essentials/cloud-storage-lifecycle-lab

gsutil lifecycle set delete-after-two-years.json gs://pkammas-bucket1

```
