# Python with Docker Example

This is a simple example demonstrating how to run a Python script using Docker.

## Prerequisites

- Docker installed on your system

## Project Structure


- `Dockerfile`: Defines the Docker image configuration.
- `app.py`: A simple Python script that prints "Hello Docker World".

## Dockerfile Overview

The `Dockerfile` contains the following commands:

```Dockerfile
FROM python:3.9
WORKDIR /app
COPY . /app
CMD [ "python3", "app.py" ]
```

FROM python:3.9: Specifies the base image for Python version 3.9.
WORKDIR /app: Sets the working directory inside the container to /app.
COPY . /app: Copies the current directory contents into /app inside the container.
CMD [ "python3", "app.py" ]: Specifies the command to run the Python script.

Running the Application
Build the Docker Image

Run the following command in your terminal to build the Docker image:

```
docker build -t python-docker-example .
```
This command will create a Docker image with the name python-docker-example.

Run the Docker Container

After building the image, run a container from the image:

```
docker run python-docker-example
```
This command will execute the app.py script inside the container, and you should see the following output:

```
Hello Docker World
```
### Notes
You can modify app.py to include other functionality and rebuild the Docker image to run the updated code.
To stop the container, use docker ps to find the running container ID and use docker stop <container_id>.
