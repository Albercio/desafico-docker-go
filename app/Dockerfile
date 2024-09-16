FROM golang:1.21-alpine as builder

WORKDIR /app

COPY . .

RUN go build -v -o /usr/local/bin/app ./...

FROM scratch

COPY --from=builder  /usr/local/bin/app /usr/local/bin/app

CMD ["/usr/local/bin/app"]
