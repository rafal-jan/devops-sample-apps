FROM golang:1.22.4 as builder
WORKDIR /app
COPY *.go ./
RUN CGO_ENABLED=0 GOOS=linux go build -o /app/server ./main.go


FROM scratch
WORKDIR /app
COPY --from=builder /app/server .
CMD ["/app/server"]