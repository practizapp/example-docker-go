# Base image is in https://registry.hub.docker.com/_/golang/
# Refer to https://blog.golang.org/docker for usage
FROM golang:1.18-alpine

WORKDIR /app

COPY go.mod ./
COPY go.sum ./

# Install dependency
RUN go mod download

# Add main.go to dir inside container
ADD src/ ./

# Build sample app
RUN go build -o /go-bee-sample-app

# Expose port to public
EXPOSE 8080
EXPOSE 443

# Copy the source code from current directory to / in container
# Place the Dockerfile into source code directory and build Docker image

# Launch Beego when the container is created
CMD [ "/go-bee-sample-app" ]