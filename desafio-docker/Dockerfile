FROM golang:1.19.2-bullseye

WORKDIR /app

COPY main.go .

RUN go mod init fullcycle
RUN go mod download

RUN go build -o main .

CMD ["./main"]