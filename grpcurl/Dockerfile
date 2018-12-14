FROM golang:alpine

RUN apk add --update openssl-dev pcre-dev git

RUN go get github.com/fullstorydev/grpcurl && \
    go install github.com/fullstorydev/grpcurl/cmd/grpcurl

ENTRYPOINT ["grpcurl"]
