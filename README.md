# payment

This is a sample GoLang app for payments

## Endpoints

**App is running on port 8080**

There are 3 endpoints:

- GET `/payment/:id` - retrieve payment by id
- POST `/payment` - create a new payment
    body json:
    ```json
    {
        "reference": "1",
        "volume": "1000.20",
        "currency": "USD"
    }
    ```

## How to build

### Host

1. Check if you have go `go version` or install it
2. Run `go build .`. The file will be located in this dir `payment` or you can run `go build -o <bin-name>` to output binary with different name

### Dockerfile

1. Use `golang:1.24.2` as a base image for build
2. Copy `go.mod` and `go.sum` and run `go mod download`
3. Copy all files inside and run `go build .` or you can run `go build -o <bin-name>` to output binary with different name
4. Prepare a running image. You can use `FROM alpine`.
5. Copy binary from build to run and configure entrypoint to just run your binary

## How to run

You need just run your binary
