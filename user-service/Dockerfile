# Golang image as base image
FROM golang:1.23.0

# set working directory inside the container
WORKDIR /app

# copy files
COPY go.mod main.go ./

# download dependencis
RUN go mod download

# copy source code into the container
COPY . .

# build the app
RUN go build -o main

# expose port
EXPOSE 8081

# Command to run
CMD ["./main"]
