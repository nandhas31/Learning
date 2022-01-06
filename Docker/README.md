# Docker

### Key Concepts

- **Dockerfile**: Specifies the instructions to build your app in a container
 
  - In this example, two separate images are used. The first one is used to build a jar file from the source files. The second one contains only the jar file so it can be distributed without have unneeded source files
  - A base image with java and maven install is used in the first line as the starting point to our construction 
  
- **Docker-Compose.yml**: Specifies how to run the container

    - `docker compose up` and `docker compose down` will start and stop the containers