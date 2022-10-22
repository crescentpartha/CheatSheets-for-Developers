## Table of Contents

- [Docker CheatSheet for Developers](#docker-cheatsheet-for-developers)
  - [Manage Containers](#manage-containers)
  - [Manage Images](#manage-images)
  - [Info and Stats](#info-and-stats)

# Docker CheatSheet for Developers

## Manage Containers

| Command                                | Description                              |
| -------------------------------------- | ---------------------------------------- |
| `docker ps`                            | Show a list of running containers        |
| `docker ps -a`                         | Show a list of all containers            |
| `docker rm CONTAINER`                  | Delete a container                       |
| `docker rm -f CONTAINER`               | Delete a running container               |
| `docker CONTAINER prune`               | Delete stopped containers                |
| `docker stop CONTAINER`                | Stop a running container                 |
| `docker start CONTAINER`               | Start a stopped container                |
| `docker cp CONTAINER:SOURCE TARGET`    | Copy a file from a container to the host |
| `docker cp CONTAINER:SOURCE TARGET`    | Copy a file from a container to the host |
| `docker cp TARGET CONTAINER:SOURCE`    | Copy a file from the host to a container |
| `docker exec -it CONTAINER EXECUTABLE` | Start a shell inside a running container |
| `docker rename OLD_NAME NEW_NAME`      | Rename a container                       |
| `docker commit CONTAINER`              | Create an image out of a container       |

**[🔼Back to Top](#table-of-contents)**

## Manage Images

| Command                           | Description                              |
| --------------------------------- | ---------------------------------------- |
| `docker pull IMAGE[:TAG]`         | Download an image                        |
| `docker push IMAGE`               | Upload an image to a repository          |
| `docker rmi IMAGE`                | Delete an image                          |
| `docker images`                   | Show list of all images                  |
| `docker image prune`              | Delete dangling images                   |
| `docker image prune -a`           | Delete all unused images                 |
| `docker build DIRECTORY`          | Build an image from a Dockerfile         |
| `docker tag IMAGE NEWIMAGE`       | Tag an image                             |
| `docker build -t IMAGE DIRECTORY` | Build and tag an image from a Dockerfile |
| `docker save IMAGE > FILE`        | Save an image to a .tar file             |
| `docker load -i TARFILE`          | Load an image from a .tar file           |

**[🔼Back to Top](#table-of-contents)**

## Info and Stats

| Command                 | Description                            |
| ----------------------- | -------------------------------------- |
| `docker logs CONTAINER` | Show the logs of a container           |
| `docker stats`          | Show stats of a running container      |
| `docker top CONTAINER`  | Show processes of a container          |
| `docker version`        | Show installed docker version          |
| `docker inspect NAME`   | Get detailed info about an object      |
| `docker diff CONTAINER` | Show all modified files in a container |
| `docker port CONTAINER` | Show mapped ports of a container       |

**[🔼Back to Top](#table-of-contents)**

