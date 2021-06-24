# Copy Files from Docker Container to Host



To copy files from a Docker container to the host use this command

```shell
docker cp <container-id>:/file/path/within/container /host/path/target
```

the `container-id` can be found by running

```shell
docker ps -al
```

