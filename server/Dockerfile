ARG ALPINE_VERSION=3.18
ARG GOLANG_VERSION=1.20
ARG COMPILER=golang:${GOLANG_VERSION}-alpine${ALPINE_VERSION}
ARG CGO_ENABLED=0

FROM ${COMPILER} AS build
RUN apk update

WORKDIR /app
COPY  . .
RUN go build -o server cmd/server/main.go

EXPOSE 8080
ENTRYPOINT ["./server"]
CMD ["8080"]
