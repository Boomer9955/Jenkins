FROM jenkinsci/blueocean

USER root

RUN apk add --no-cache py-pip musl-dev python3-dev libffi-dev openssl-dev cargo gcc libc-dev make \
    && pip3 install docker-compose \
    && pip install ansible \
    && pip install helm-python 
    
RUN apk add --update --no-cache wget git && \
    wget https://get.helm.sh/helm-canary-linux-amd64.tar.gz -O - | tar -xz && \
    mv linux-amd64/helm /usr/bin/helm && \
    chmod +x /usr/bin/helm && \
    rm -rf linux-amd64

RUN chmod +x /usr/bin/helm

USER jenkins