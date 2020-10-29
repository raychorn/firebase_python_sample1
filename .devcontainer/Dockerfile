ARG DEBIAN_FRONTEND=noninteractive
FROM raychorn/ubuntu_python38

ENV APP_PATH=/workspaces/python-firebase-sample1

LABEL version="1.0"
LABEL maintaner="Ray C Horn (raychorn@gmail.com)"
LABEL release-date="10-28-2020"
LABEL promoted="true"

RUN apt-get update && apt-get install -y -q --no-install-recommends \
    apt-transport-https \
    build-essential \
    ca-certificates \
    curl \
    git \
    libssl-dev \
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata expect

RUN git --version && \
    git config --global user.email "raychorn@gmail.com" && \
    git config --global user.name "Ray C Horn" 

RUN ln -s /usr/bin/python3.8 /usr/bin/python && \
    ln -s /usr/bin/pip3 /usr/bin/pip

RUN TZ=US/Mountain \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN export dir=$(pwd) && \
    echo $dir && \
    cd /root && \
    wget https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-316.0.0-linux-x86_64.tar.gz && \
    tar -xvzf google-cloud-sdk-316.0.0-linux-x86_64.tar.gz

RUN /workspaces/python-firebase-sample1/install-gcloud.sh
