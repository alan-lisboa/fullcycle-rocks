FROM golang:alpine AS Build

WORKDIR /go/src/app
COPY . .
RUN go build -o hello

FROM scratch AS app
COPY --from=Build /go/src/app /
CMD ["./hello"]