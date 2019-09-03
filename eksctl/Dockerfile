FROM alpine:3.10

RUN apk add --update openssl-dev curl

RUN curl -sS -LO "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz

ENTRYPOINT ["./eksctl"]
