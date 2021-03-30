# Triggering a Cloud Function with Cloud Pub/Sub
Check APIs are enabled (APIs-> Library->Pub/Sub and Functions)
Create Pub/Sub Topic (Big Data -> Pub/Sub-> Create Topic)
Create function (Compute -> Google Cloud Functions -> Create Function - trigger CloudPub/Sub instead of Http  /Python)
Write src code to send
```
import base64

def greetings_pubsub(data, context):

    if 'data' in data:
        name = base64.b64decode(data['data']).decode('utf-8')
    else:
        name = 'folks'
    print('Greetings {} from Linux Academy!'.format(name))
```
function to execute: greetings_pubsub

Publish message to topic to test can be verified from Logs of Function

Cloud shell - Trigger Cloud Function directly from command line.
```
DATA=$(printf 'my friends' | base64)

gcloud functions call la-pubsub-function --data '{"data":"'$DATA'"}'
```

Cloud shell - Publish message to topic from command line.
```
DATA=$(printf 'my friends' | base64)

gcloud pubsub topics publish greetings --message "y'all"
```