FROM alpine:3.10

RUN apk add --update openssl-dev curl

RUN curl -sS -LO https://github.com/GoogleCloudPlatform/terraformer/releases/download/$(curl -s https://api.github.com/repos/GoogleCloudPlatform/terraformer/releases/latest | grep tag_name | cut -d '"' -f 4)/terraformer-linux-amd64 && \
    chmod +x terraformer-linux-amd64 && \
    curl -sS -LO https://releases.hashicorp.com/terraform-provider-aws/2.26.0/terraform-provider-aws_2.26.0_linux_amd64.zip && \
    unzip terraform-provider-aws_2.26.0_linux_amd64.zip && \
    mkdir -p .terraform.d/plugins/linux_amd64 && \
    cp ./terraform-provider-aws_v2.26.0_x4 ./.terraform.d/plugins/linux_amd64/terraform-provider-aws_v2.26.0_x4

ENTRYPOINT ["./terraformer-linux-amd64"]
