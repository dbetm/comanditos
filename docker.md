## Docker

### Images

**Pull an image from Docker Hub**
```bash
docker pull <name>
docker pull <name:tag>
```

**Download an image and run it in a container as a daemon**
```bash
docker run -d <image-name:tag> (Tag is optional)
```

**List images**
```bash
docker images
```

**Delete images**
```bash
docker rmi <image-id>
docker rmi <image_name:tag>
```

**Delete all images**
```bash
docker rmi $(docker images)
```

### Containers (an image is running)

**List containers**
```bash
docker ps
docker ps -a (include containers with all status)
```

**Delete a container**
```bash
docker rm <container-id>
docker rm <container-name>
docker rm -f <container-id> (force deletion when container is up)
```

**Delete all container with status `exited`**
```bash
docker rm $(docker ps --filter status=exited -q)
```

**Run container**
```bash
docker run <container-name> --name <a-name> (name is optional)
```

**Run container passing env's and as daemons**
```bash
docker run -d -e ENV_NAME=VAL <container-name>
```

**Stop container**
```bash
docker stop <container-id>
```

**Star a container after stopped status**
```bash
docker start <container-id>
```

**Restart a container**
```bash
docker restart <container-id>
```

**Start an interactive session**
```bash
docker exec -it <container-id> [entry-point] (entrypoint could be `bash`)
```

**Check logs**
```bash
docker logs -follow <container-id> (follow for autoscroll)
docker logs <container-name>
```


**Rename a container**
```bash
docker rename CONTAINER_OLD_NAME NEW_NAME
```

**Check stats**
```bash
docker stats
```
