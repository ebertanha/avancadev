FROM golang:1.15

WORKDIR /go/src/fullcycle-a

COPY . . 

# Install go dependencies
RUN go get github.com/joho/godotenv && \
    go get github.com/wesleywillians/go-rabbitmq/queue

RUN GOOS=linux go build

EXPOSE 9090

ENTRYPOINT [ "./fullcycle-a" ]