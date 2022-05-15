FROM golang:1.18-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./

RUN go mod download


ADD src/ ./

RUN go build -o /go-gin-sample-app

CMD [ "/go-gin-sample-app" ]