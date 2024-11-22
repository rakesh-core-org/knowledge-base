unable to connect to ollama server via open-webui running in docker 

1. **Check Docker Container Status**: Ensure that your Docker container is running. You can check this by executing `docker ps` in your terminal. Look for the container running Open-WebUI.

2. **Install Docker**: Make sure Docker is installed on your system. You can download and install it from [Docker's official website](https://www.docker.com/products/docker-desktop).

3. **Pull the Ollama Docker Image**: Open a terminal or command prompt and pull the Ollama image by running:
   ```bash
   docker pull ollama/ollama:latest
