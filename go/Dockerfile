FROM golang:1.16.3-alpine3.13 AS build 

RUN mkdir -p /go/src/helloworld
WORKDIR /go/src/helloworld

COPY hello.go /go/src/helloworld
RUN go build hello.go

FROM scratch
COPY --from=build /go/src/helloworld /
CMD ["./hello"]