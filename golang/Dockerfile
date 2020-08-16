FROM golang:1.14.7-alpine3.11 as builder

WORKDIR /
COPY . .
RUN go build hello-go.go

WORKDIR /
FROM scratch 
COPY --from=builder ./hello-go / 

CMD [ "/hello-go" ]

