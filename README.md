# Simple Docker Hello Captain

This project provides a basic `Dockerfile` that uses Alpine Linux to print "Hello, Captain!" when the container is run. It's a minimal example to demonstrate how to create and run a Docker image.

## Features

- Uses the lightweight **Alpine Linux** base image.
- Prints **"Hello, Captain!"** to the console when the container starts.
- Ideal for Docker beginners due to its simplicity.

## Prerequisites

- **Docker** installed on your machine. Download it from [Docker's official website](https://www.docker.com/get-started) if needed.

## Installation

1. **Create a project directory** (or clone this repository):
   ```bash
   mkdir Basic-Dockerfile-roadmap.sh
   cd Basic-Dockerfile-roadmap.sh
   ```

2. **Add the `Dockerfile`**:
   Create a file named `Dockerfile` in the project directory with the following content:
   ```dockerfile
   # Use the official lightweight Alpine Linux image as the base image
   FROM alpine:latest

   # Use the CMD instruction to print "Hello, Captain!" and exit
   CMD echo "Hello, Captain!"
   ```

## Usage

1. **Build the Docker image**:
   In the terminal, navigate to the directory with the `Dockerfile` and run:
   ```bash
   docker build -t hello-captain .
   ```
   - `-t hello-captain` names the image "hello-captain".
   - `.` uses the current directory as the build context.

2. **Run the Docker container**:
   ```bash
   docker run hello-captain
   ```
   This launches the container, prints the message, and exits.

### Expected Output:
```
Hello, Captain!
```

## Explanation

- **Base Image**: `FROM alpine:latest` uses the latest Alpine Linux, a lightweight and efficient base image for simple containers.
- **Command**: `CMD echo "Hello, Captain!"` defines the default action, printing the message to the console when the container runs.

## Troubleshooting

- **Docker Not Installed**: Verify Docker is installed with `docker --version`.
- **Permission Errors**: On Linux, use `sudo` with Docker commands or add your user to the `docker` group.
- **Build Fails**: Ensure the `Dockerfile` is correctly formatted and located in the current directory.
