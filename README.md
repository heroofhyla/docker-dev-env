To use the container for development, use this command from the root of the
target web app.

docker run -v "$PWD":/app -tid -p 8888:80 aezart/dev-environment
