FROM golang:1.18 as builder

COPY . /mqttcli
WORKDIR /mqttcli

RUN go mod tidy
RUN go build

FROM debian:bookworm-slim
COPY --from=builder /mqttcli/mqttcli /