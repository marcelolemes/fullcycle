FROM golang:1.20-alpine3.18 as builder

WORKDIR /app

COPY main.go .

RUN CGO_ENABLED=0 go build -o /main main.go

FROM scratch

WORKDIR /

COPY --from=builder /main /main

EXPOSE 8080

ENTRYPOINT ["/main"]