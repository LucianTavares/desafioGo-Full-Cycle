FROM golang:1.7.3-alpine as build 

WORKDIR /usr/src/desafio

COPY . .

RUN go build -o desafio

FROM scratch

WORKDIR /usr/src/desafio

COPY --from=build /usr/src/desafio .

CMD ["./desafio"]