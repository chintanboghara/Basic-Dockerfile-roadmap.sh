Here is a basic `Dockerfile` that fulfills the requirements:

```dockerfile
# Use the official lightweight Alpine Linux image as the base image
FROM alpine:latest

# Use the CMD instruction to print "Hello, Captain!" and exit
CMD echo "Hello, Captain!"
```

### Explanation:
1. **Base Image**: `FROM alpine:latest` specifies that the base image is the latest version of Alpine Linux, which is lightweight and suitable for simple tasks.
2. **Command**: `CMD echo "Hello, Captain!"` sets the default command to print "Hello, Captain!" to the console when the container is run.

### Steps to Build and Run the Docker Image:
1. Save the `Dockerfile` in the root directory of project.
2. Open a terminal and navigate to the directory containing the `Dockerfile`.
3. Build the Docker image:
   ```bash
   docker build -t hello-captain .
   ```
4. Run the Docker container:
   ```bash
   docker run hello-captain
   ```

You should see the output:
```
Hello, Captain!
```
