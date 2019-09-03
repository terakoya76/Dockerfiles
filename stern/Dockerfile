FROM alpine:3.10

RUN apk add --update openssl-dev curl wget jq

RUN SYSNAME="$(uname -s | tr '[A-Z]' '[a-z]')_amd64" && \
    curl -sS https://api.github.com/repos/wercker/stern/releases/latest | jq -r --arg SYSNAME "$SYSNAME" '.assets[] | select(.name | contains($SYSNAME)) | .browser_download_url' | wget -qi - && \
    mv "stern_$SYSNAME" stern && \
    chmod +x ./stern

ENTRYPOINT ["./stern"]
