FROM ubuntu:20.04

ENV PATH $PATH:/usr/local/gcloud/google-cloud-sdk/bin

RUN apt-get update && apt-get install curl -y
RUN apt-get install -y python-is-python3 && apt-get install -y python3-pip
RUN curl https://dl.google.com/dl/cloudsdk/release/google-cloud-sdk.tar.gz > /tmp/google-cloud-sdk.tar.gz
RUN mkdir -p /usr/local/gcloud \
  && tar -C /usr/local/gcloud -xvf /tmp/google-cloud-sdk.tar.gz \
  && /usr/local/gcloud/google-cloud-sdk/install.sh

COPY echo.sh /opt/echo.sh

ENTRYPOINT bash /opt/echo.sh