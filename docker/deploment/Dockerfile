FROM jenkinsci/blueocean

USER root

RUN apk add --no-cache py-pip musl-dev python3-dev libffi-dev openssl-dev cargo gcc libc-dev make \
    && pip3 install docker-compose \
    && pip install ansible

USER jenkins