# BUILD
FROM golang:1.9.1-alpine3.6 as builder

COPY dispatcher.go .
RUN go build dispatcher.go

# RUN
FROM alpine:edge
EXPOSE 80
CMD ["/dispatcher"]

COPY --from=builder /go/dispatcher /
COPY static /static/

FROM debian:jessie-slim
RUN apt-get update && apt-get -y install ca-certificates
ADD httFROM debian:jessie-slimps://get.aquasec.com/microscanner /
RUN chmod +x /microscanner
RUN /microscanner ${token} [--continue-on-failure]
