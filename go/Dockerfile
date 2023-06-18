# syntax=docker/dockerfile:1

FROM golang:1.18-alpine

WORKDIR /app

COPY ./go/go.mod ./
COPY ./go/go.sum ./
RUN go mod download

COPY ./go ./

WORKDIR /app/src

RUN go build -o /safefetch

EXPOSE 4501

CMD [ "/safefetch" ]