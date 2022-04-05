I'm working on learning Docker right now, and trying understand how to integrate
it into my development workflow with minimal hassle.

Use `make` to build the image.

To use the container for development, use this command from the root of the
target web app.

```
docker run -v "$PWD":/app -tid -p 8888:80 aezart/dev-environment
```

To build a containerized version of your web app, include this in the app's
Dockerfile:

```
FROM aezart/dev-environment
WORKDIR /app
COPY . .
```
