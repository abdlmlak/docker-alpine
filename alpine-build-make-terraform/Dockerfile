FROM bhuisgen/alpine-build-make:latest
MAINTAINER Boris HUISGEN <bhuisgen@hbis.fr>

ENV TERRAFORM_VERSION=0.9.11

RUN apk add --update zip && \
    curl -sSL https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip -o /tmp/terraform.zip && \
    unzip /tmp/terraform.zip -d /usr/bin && \
    rm /tmp/terraform.zip && \
    apk del zip && \
    rm -rf /var/cache/apk/*
