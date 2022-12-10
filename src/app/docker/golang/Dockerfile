# Specify the base image for the go app.
FROM golang:1.15

WORKDIR /go/src/github.com/postgres-go
# Copy everything from this project into the filesystem of the container.
COPY . .
# Obtain the package needed to run code. Alternatively use GO Modules. 
RUN go get -u github.com/lib/pq

WORKDIR /go/src/yuta/go
# Add the contents of the host OS . /go contents to the working directory
ADD ./go .