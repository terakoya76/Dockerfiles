FROM alpine:3.10

RUN apk add --update openssl-dev curl

RUN curl -sS -LO https://github.com/flosell/iam-policy-json-to-terraform/releases/download/1.2.0/iam-policy-json-to-terraform_alpine && \
    chmod +x ./iam-policy-json-to-terraform_alpine

ENTRYPOINT ["./iam-policy-json-to-terraform_alpine"]
