FROM alpine:3.10

RUN apk add --update openssl-dev curl

RUN curl -sS -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && \
    chmod +x ./kubectl

ENTRYPOINT ["./kubectl"]
