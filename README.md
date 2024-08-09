### DOCKER

Here’s a Docker cheat sheet tailored for beginners, with key commands and their descriptions:

### **1. Docker Basics**

- **`docker --version`**: Check the Docker version installed.
- **`docker info`**: Display system-wide information like the number of containers, images, etc.

### **2. Docker Images**

- **`docker images`**: List all Docker images on your system.
- **`docker pull <image>`**: Download an image from Docker Hub.
- **`docker build -t <image_name> .`**: Build an image from a Dockerfile in the current directory.
- **`docker rmi <image_id>`**: Remove a Docker image.

### **3. Docker Containers**

- **`docker ps`**: List all running containers.
- **`docker ps -a`**: List all containers (running and stopped).
- **`docker run <image>`**: Create and start a container from an image.
- **`docker run -d <image>`**: Run a container in detached mode (in the background).
- **`docker run -it <image>`**: Run a container in interactive mode (with a shell).
- **`docker stop <container_id>`**: Stop a running container.
- **`docker start <container_id>`**: Start a stopped container.
- **`docker rm <container_id>`**: Remove a stopped container.

### **4. Docker Volumes**

- **`docker volume create <volume_name>`**: Create a new volume.
- **`docker volume ls`**: List all volumes.
- **`docker volume rm <volume_name>`**: Remove a volume.
- **`docker run -v <volume_name>:/path/in/container <image>`**: Mount a volume to a container.

### **5. Docker Networks**

- **`docker network ls`**: List all Docker networks.
- **`docker network create <network_name>`**: Create a custom network.
- **`docker network connect <network_name> <container_id>`**: Connect a container to a network.
- **`docker network disconnect <network_name> <container_id>`**: Disconnect a container from a network.

### **6. Docker Compose**

- **`docker-compose up`**: Create and start containers defined in a `docker-compose.yml` file.
- **`docker-compose down`**: Stop and remove containers, networks, and volumes created by `docker-compose up`.
- **`docker-compose build`**: Build or rebuild services.

### **7. Docker Cleanup**

- **`docker system prune`**: Remove all stopped containers, unused networks, and dangling images.
- **`docker container prune`**: Remove all stopped containers.
- **`docker image prune`**: Remove unused images.

### **8. Docker Logs & Monitoring**

- **`docker logs <container_id>`**: View logs of a specific container.
- **`docker stats`**: Display a live stream of resource usage statistics for all containers.

### **9. Docker Registry**

- **`docker login`**: Log in to a Docker registry (e.g., Docker Hub).
- **`docker tag <image> <username>/<repository>:<tag>`**: Tag an image for a specific repository.
- **`docker push <username>/<repository>:<tag>`**: Push an image to a Docker registry.
- **`docker pull <username>/<repository>:<tag>`**: Pull an image from a Docker registry.

### **10. Dockerfile Basics**

- **`FROM <base_image>`**: Specify the base image.
- **`COPY <src> <dest>`**: Copy files or directories to the container.
- **`RUN <command>`**: Execute a command in the container.
- **`CMD <command>`**: Provide the default command to run the container.

This cheat sheet covers the essential commands you’ll use frequently as a beginner in Docker. As you gain more experience, you'll discover more advanced commands and features!
