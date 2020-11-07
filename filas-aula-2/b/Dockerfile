FROM golang:1.15

WORKDIR /go/src/fullcycle-b

COPY . . 

# Install go dependencies
RUN go get github.com/joho/godotenv && \
    go get github.com/satori/go.uuid && \
    go get github.com/streadway/amqp && \
    go get github.com/wesleywillians/go-rabbitmq/queue

RUN GOOS=linux go build

EXPOSE 9091

ENTRYPOINT [ "./fullcycle-b" ]