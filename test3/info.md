## Push to dockerhub

1. docker login
2. docker tag imagename  [dockerhubuser/]imagename[:TAG]
3.docker push [dockerhubuser/]imagename[:TAG]

## Push to GCP 

1. gcloud auth configure-docker
2. docker tag imagename gcr.io/projectid/imagename:latest
3. gcloud docker -- push gcr.io/projectid/imagename:latest

## Push to artifacts
1. create a repo in artifacts
2. run gcloud auth configure-docker \
    us-central1-docker.pkg.dev
3. docker tag image:tag us-central1-docker.pkg.dev/projectID/repo/image:tag
4. docker push us-central1-docker.pkg.dev/projectID/repo/image:tag

## Pull
docker pull us-central1-docker.pkg.dev/projectID/repo/image:tag
