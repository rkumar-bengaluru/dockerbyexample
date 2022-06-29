# syntax=docker/dockerfile:1

FROM golang:1.16-alpine
WORKDIR /app 
COPY **.mod .
RUN go mod download
ADD . .
RUN go mod download
RUN go build -o /docker-go-server ./cmd
EXPOSE 8080
CMD [ "/docker-go-server" ]