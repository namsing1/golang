FROM golang:1.15-alpine AS GO_BUILD
COPY . /rest-service
WORKDIR /rest-service/rest-service
RUN go build -o /go/bin/rest-service/rest-service
FROM alpine:3.10
WORKDIR app
COPY --from=GO_BUILD /go/bin/rest-service/ ./
EXPOSE 8080
CMD ["./rest-service"]