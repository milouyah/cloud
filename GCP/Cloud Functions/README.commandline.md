# Hello World
### 1. Create a function
index.js
### 2. Create a cloud storage bucket

```
gsutil mb -p [PROJECT_ID] gs://[BUCKET_NAME]
```
Deploy your function

### 3. Deploy your function
When deploying a new function, you must specify --trigger-topic, --trigger-bucket, or --trigger-http. When deploying an update to an existing function, the function keeps the existing trigger unless otherwise specified.
<br>
For this lab, you'll set the --trigger-topic as hello_world.
```
gcloud functions deploy helloWorld \
  --stage-bucket [BUCKET_NAME] \
  --trigger-topic hello_world \
  --runtime nodejs8
```
<br>
```
gcloud functions describe helloWorld
```

### 4. Test the function
DATA=$(printf 'Hello World!'|base64) && gcloud functions call helloWorld --data '{"data":"'$DATA'"}'




* 참고
* [Pub/Sub: Google 규모의 메시징 서비스 ](https://cloud.google.com/pubsub/architecture)
* [Background function](https://cloud.google.com/functions/docs/writing/background)