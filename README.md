### DOCKER

Here’s a Docker cheat sheet tailored for beginners, with key commands and their descriptions:

---

### **1. Docker Basics**

- **`docker --version`**: Check the Docker version installed.

  - **Example:** `docker --version`
    - Output: `Docker version 20.10.7, build f0df350`

- **`docker info`**: Display system-wide information like the number of containers, images, etc.

  - **Example:** `docker info`
    - Output includes system status, number of containers, images, etc.

- **`docker help`**: Get help for Docker commands.
  - **Example:** `docker help`
    - Displays a list of available Docker commands and options.

---

### **2. Docker Images**

- **`docker images`**: List all Docker images on your system.

  - **Example:** `docker images`
    - Output: A list of all images with repository name, tag, image ID, and size.

- **`docker pull <image>`**: Download an image from Docker Hub.

  - **Example:** `docker pull nginx`
    - Downloads the latest version of the `nginx` image.

- **`docker build -t <image_name> .`**: Build an image from a Dockerfile in the current directory.

  - **Example:** `docker build -t myapp:1.0 .`
    - Builds an image named `myapp` with the tag `1.0`.

- **`docker rmi <image_id>`**: Remove a Docker image.

  - **Example:** `docker rmi 7d9495d03763`
    - Removes the image with ID `7d9495d03763`.

- **`docker tag <image_id> <new_tag>`**: Create a new tag for an image.
  - **Example:** `docker tag nginx:latest myrepo/nginx:v1`
    - Tags the `nginx:latest` image as `myrepo/nginx:v1`.

---

### **3. Docker Containers**

- **`docker ps`**: List all running containers.

  - **Example:** `docker ps`
    - Output: A list of running containers with details like container ID, image name, and status.

- **`docker ps -a`**: List all containers (running and stopped).

  - **Example:** `docker ps -a`
    - Output: A list of all containers, including stopped ones.

- **`docker run <image>`**: Create and start a container from an image.

  - **Example:** `docker run nginx`
    - Creates and starts a container from the `nginx` image.

- **`docker run -d <image>`**: Run a container in detached mode (in the background).

  - **Example:** `docker run -d nginx`
    - Runs the `nginx` container in the background.

- **`docker run -it <image>`**: Run a container in interactive mode (with a shell).

  - **Example:** `docker run -it ubuntu /bin/bash`
    - Starts an Ubuntu container with an interactive Bash shell.

- **`docker stop <container_id>`**: Stop a running container.

  - **Example:** `docker stop 5d5f3b9a5173`
    - Stops the container with ID `5d5f3b9a5173`.

- **`docker start <container_id>`**: Start a stopped container.

  - **Example:** `docker start 5d5f3b9a5173`
    - Starts the container with ID `5d5f3b9a5173`.

- **`docker restart <container_id>`**: Restart a running container.

  - **Example:** `docker restart 5d5f3b9a5173`
    - Restarts the container with ID `5d5f3b9a5173`.

- **`docker rm <container_id>`**: Remove a stopped container.

  - **Example:** `docker rm 5d5f3b9a5173`
    - Removes the container with ID `5d5f3b9a5173`.

- **`docker exec -it <container_id> <command>`**: Run a command inside a running container.
  - **Example:** `docker exec -it 5d5f3b9a5173 /bin/bash`
    - Opens a Bash shell inside the container.

---

### **4. Docker Volumes**

- **`docker volume create <volume_name>`**: Create a new volume.

  - **Example:** `docker volume create my_volume`
    - Creates a volume named `my_volume`.

- **`docker volume ls`**: List all volumes.

  - **Example:** `docker volume ls`
    - Lists all Docker volumes.

- **`docker volume rm <volume_name>`**: Remove a volume.

  - **Example:** `docker volume rm my_volume`
    - Removes the volume named `my_volume`.

- **`docker run -v <volume_name>:/path/in/container <image>`**: Mount a volume to a container.

  - **Example:** `docker run -v my_volume:/app nginx`
    - Mounts the `my_volume` volume to the `/app` directory inside the `nginx` container.

- **`docker volume inspect <volume_name>`**: Display detailed information about a volume.
  - **Example:** `docker volume inspect my_volume`
    - Provides details about the `my_volume` volume, such as mount point and driver.

---

### **5. Docker Networks**

- **`docker network ls`**: List all Docker networks.

  - **Example:** `docker network ls`
    - Lists all networks managed by Docker.

- **`docker network create <network_name>`**: Create a custom network.

  - **Example:** `docker network create my_network`
    - Creates a network named `my_network`.

- **`docker network connect <network_name> <container_id>`**: Connect a container to a network.

  - **Example:** `docker network connect my_network 5d5f3b9a5173`
    - Connects the container with ID `5d5f3b9a5173` to the `my_network` network.

- **`docker network disconnect <network_name> <container_id>`**: Disconnect a container from a network.

  - **Example:** `docker network disconnect my_network 5d5f3b9a5173`
    - Disconnects the container with ID `5d5f3b9a5173` from the `my_network` network.

- **`docker network inspect <network_name>`**: Display detailed information about a network.

  - **Example:** `docker network inspect my_network`
    - Provides details about the `my_network` network, such as connected containers and IP addresses.

- **`docker run --network <network_name> <image>`**: Run a container on a specific network.
  - **Example:** `docker run --network my_network nginx`
    - Runs the `nginx` container on the `my_network` network.

---

### **6. Docker Compose**

- **`docker-compose up`**: Create and start containers defined in a `docker-compose.yml` file.

  - **Example:** `docker-compose up`
    - Starts all services defined in the `docker-compose.yml` file.

- **`docker-compose down`**: Stop and remove containers, networks, and volumes created by `docker-compose up`.

  - **Example:** `docker-compose down`
    - Stops and removes all containers, networks, and volumes.

- **`docker-compose build`**: Build or rebuild services.

  - **Example:** `docker-compose build`
    - Builds all services defined in the `docker-compose.yml` file.

- **`docker-compose logs`**: View output from containers.

  - **Example:** `docker-compose logs`
    - Displays logs from all containers defined in the `docker-compose.yml` file.

- **`docker-compose ps`**: List containers.

  - **Example:** `docker-compose ps`
    - Lists all containers created by Docker Compose.

- **`docker-compose stop`**: Stop running containers without removing them.
  - **Example:** `docker-compose stop`
    - Stops all running containers defined in the `docker-compose.yml` file.

---

### **7. Docker Cleanup**

- **`docker system prune`**: Remove all stopped containers, unused networks, and dangling images.

  - **Example:** `docker system prune -f`
    - Forcefully prunes the system, removing all stopped containers, unused networks, and dangling images.

- **`docker container prune`**: Remove all stopped containers.

  - **Example:** `docker container prune`
    - Removes all stopped containers.

- **`docker image prune`**: Remove unused images.

  - **Example:** `docker image prune -a`
    - Removes all unused images, including dangling and unreferenced ones.

- **`docker volume prune`**: Remove all unused volumes.
  - **Example:** `docker volume prune`
    - Removes all unused Docker volumes.

---

### **8. Docker Logs & Monitoring**

- **`docker logs <container_id>`**: View logs of a specific container.

  - **Example:** `docker logs 5d5f3b9a5173`
    - Displays the logs for the container with ID `5d5f3b9a5173`.

- **`docker stats`**: Display a live stream of resource usage statistics for all containers.
  - **Example:** `docker stats`
    - Shows real-time statistics for CPU, memory, network, and disk I/O for running containers.

---

### **8. Docker Logs & Monitoring**

- **`docker logs <container_id>`**: View logs of a specific container.

  - **Example:** `docker logs 5d5f3b9a5173`
    - Displays the logs for the container with ID `5d5f3b9a5173`.

- **`docker stats`**: Display a live stream of resource usage statistics for all containers.

  - **Example:** `docker stats`
    - Shows real-time statistics for CPU, memory, network, and disk I/O for running containers.

- **`docker top <container_id>`**: Display the running processes of a container.

  - **Example:** `docker top 5d5f3b9a5173`
    - Lists the processes running inside the container with ID `5d5f3b9a5173`.

- **`docker inspect <container_id>`**: Return detailed information on a container or image.
  - **Example:** `docker inspect 5d5f3b9a5173`
    - Outputs detailed JSON information about the container, such as its configuration and state.

---

### **9. Docker Registry**

- **`docker login`**: Log in to a Docker registry (e.g., Docker Hub).

  - **Example:** `docker login`
    - Prompts for Docker Hub credentials to log in.

- **`docker tag <image_id> <username>/<repository>:<tag>`**: Tag an image for a specific repository.

  - **Example:** `docker tag nginx:latest hazrat17/nginx:v1`
    - Tags the `nginx:latest` image as `hazrat17/nginx:v1`.

- **`docker push <username>/<repository>:<tag>`**: Push an image to a Docker registry.

  - **Example:** `docker push hazrat17/nginx:v1`
    - Pushes the `hazrat17/nginx:v1` image to Docker Hub.

- **`docker pull <username>/<repository>:<tag>`**: Pull an image from a Docker registry.

  - **Example:** `docker pull hazrat17/nginx:v1`
    - Pulls the `hazrat17/nginx:v1` image from Docker Hub.

- **`docker search <term>`**: Search Docker Hub for images matching the search term.
  - **Example:** `docker search nginx`
    - Searches Docker Hub for images related to `nginx`.

---

### **10. Dockerfile Basics**

- **`FROM <base_image>`**: Specify the base image.

  - **Example:** `FROM node:14-alpine`
    - Starts with the Node.js version 14 image on Alpine Linux.

- **`COPY <src> <dest>`**: Copy files or directories to the container.

  - **Example:** `COPY . /app`
    - Copies the current directory to `/app` inside the container.

- **`ADD <src> <dest>`**: The ADD command can do everything that COPY does, but it also includes additional functionality.

  - **Example:** `ADD my_archive.tar.gz /usr/src/app`
    - Copies the current directory to `/app` inside the container.

- **`RUN <command>`**: Execute a command in the container.

  - **Example:** `RUN npm install`
    - Installs dependencies defined in a `package.json` file.

- **`CMD <command>`**: Provide the default command to run the container.

  - **Example:** `CMD ["node", "index.js"]`
    - Specifies the command to start the Node.js application.

- **`ENTRYPOINT ["executable", "param1", "param2"]`**: Configures a container that will run as an executable.

  - **Example:** `ENTRYPOINT ["node", "index.js"]`
    - Defines the executable (`node`) and its arguments (`index.js`).

- **`EXPOSE <port>`**: Inform Docker that the container listens on the specified network ports at runtime.

  - **Example:** `EXPOSE 8080`
    - Opens port `8080` in the container.

- **`WORKDIR <path>`**: Set the working directory for any RUN, CMD, ENTRYPOINT, COPY, and ADD commands.

  - **Example:** `WORKDIR /app`
    - Sets `/app` as the working directory for subsequent commands.

- **`ENV <key>=<value>`**: Set environment variables.
  - **Example:** `ENV NODE_ENV=production`
    - Sets the `NODE_ENV` environment variable to `production`.

---

