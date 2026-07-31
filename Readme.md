# WebServer

A basic web server built in Go using only the standard library. It serves static files and exposes two simple HTTP endpoints for demonstration purposes.

## Features

- **Static file serving** — serves any files placed in the `static/` directory from the root path (`/`)
- **`GET /hello`** — a simple handler that logs a greeting to the server console
- **`POST /form`** — parses form data and echoes back the submitted `name` and `address` fields

## Requirements

- [Go](https://go.dev/dl/) 1.26 or later

## Getting Started

Clone the repository:

```bash
git clone https://github.com/medhan-sh/WebServer.git
cd WebServer
```

Run the server:

```bash
go run main.go
```

The server listens on **port 8080**. Once running, visit:

```
http://localhost:8080/
```

## Usage

### Static files

Place any HTML, CSS, JS, or other static assets inside the `static/` folder — they'll be served directly from the root path.

### `/hello`

```bash
curl http://localhost:8080/hello
```

Only `GET` requests are accepted; any other method or path returns an error.

### `/form`

Submit a form via `POST` with `name` and `address` fields:

```bash
curl -X POST http://localhost:8080/form \
  -d "name=Jane Doe" \
  -d "address=123 Main St"
```

The server responds with the parsed values.

## Project Structure

```
WebServer/
├── main.go      # Server entry point and route handlers
├── go.mod       # Go module definition
└── static/      # Static assets served at "/"
```

## License

No license has been specified for this project yet.
