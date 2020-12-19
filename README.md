# Firebase Python Project Sample 1

This project will not work at firebase so this project has been switched to GCP where this will work with the App Engine.

This projects builds the docker container you need to run the project.

To complete the installation of gcloud run the following command.
./install-gcloud.sh

The following is optional and need only be done once.  This was done to resolve the issues with pip3 because it appeared to me I was using the Python 3.8 Packages with pip3.
virtualenv -p /usr/bin/python3.7 venv

Do this when you begin using the container:
. venv/bin/activate

gcloud components install app-engine-python

Clone the Google Code Samples
git clone https://github.com/GoogleCloudPlatform/python-docs-samples

## Prerequisities

[install-google-cloud-sdk-on-ubuntu](https://stackoverflow.com/questions/56679191/apt-get-is-broken-after-install-google-cloud-sdk-on-ubuntu-18-04-lts)

1. echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
2. curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -
3. apt-get update && apt-get install google-cloud-sdk -y
4. apt-get install google-cloud-sdk-app-engine-java google-cloud-sdk-app-engine-python google-cloud-sdk-pubsub-emulator google-cloud-sdk-bigtable-emulator google-cloud-sdk-datastore-emulator -y


(c). Copyright, Ray C Horn, All Rights Reserved.