# Hello from Docker

A simple static web application served by Nginx inside a Docker container. The page displays the required message: **Hello from Docker!**

## Requirements

- Docker Desktop, or Docker Engine

## Build the image

Open a terminal in this folder and run:

```bash
docker build -t hello-from-docker .
```

## Run the container

```bash
docker run --name hello-from-docker-app -p 8080:80 hello-from-docker
```

Open [http://localhost:8080](http://localhost:8080) in a browser.

To run it in the background instead:

```bash
docker run -d --name hello-from-docker-app -p 8080:80 hello-from-docker
```

## Stop and remove the container

```bash
docker stop hello-from-docker-app
docker rm hello-from-docker-app
```

## Project files

- `Dockerfile` builds the Nginx image and includes a health check.
- `nginx.conf` configures the web server.
- `index.html` contains the simple application.
