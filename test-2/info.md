

docker run  -it -v /path/to/key:/root/.config/gcloud imagemane

###to do auth with service account : 
docker run -it -v ~/test3/tmp:/root/.config/gcloud test3 gcloud auth activate-service-account --key-file=/root/.config/gcloud/key.json

###add to docker compuse

environment:
       - name: GOOGLE_APPLICATION_CREDENTIALS
         value: /path/to/key


