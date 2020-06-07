# Docker Deployment

Salah satu cara untuk deploy aplikasi yang dibangun menggunakan bahasa pemrograman Golang adalah dengan menggunakan Docker.

Contoh script Dockerfile:

```
## Build
FROM golang:1.14.2 AS builder
RUN mkdir /app
ADD . /app
WORKDIR /app

RUN GOOS=linux GOARCH=amd64 go build -ldflags="-w -s" -a \
      -o api .

## Let's go!
FROM gcr.io/distroless/base-debian10
COPY --from=builder /app/api /usr/bin/api
EXPOSE 3000
ENTRYPOINT ["api"]

```
