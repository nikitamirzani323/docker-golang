FROM golang:alpine

RUN apk update && apk add git

ENV PORT=7176

WORKDIR /app

COPY . .

RUN go mod tidy
RUN go build -o binary

ENTRYPOINT [ "./binary" ]