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


(c). Copyright, Ray C Horn, All Rights Reserved.