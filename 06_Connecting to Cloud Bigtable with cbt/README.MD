# Connecting to Cloud Bigtable with cbt
API and Services -> Library ->Check API for BigTable is Enabled

? maybe we add first the instance from Console
```
gcloud components update

gcloud components install cbt


echo project=<PROJECT_ID> > ~/.cbtrc

echo instance=la-data-cbt >> ~/.cbtrc

cbt createtable la-table

cbt ls

cbt createfamily la-table offerings

cbt set la-table r1 offerings:c1=labs

cbt read la-table

cbt set la-table r1 offerings:c2=courses

cbt read la-table
```

