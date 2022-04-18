# Podman Machine Start Script



Use this script to check if podman machine is running and start it if not. 
It also exposes port 12979 so IntelliJ can connect to it and manage containers.

```sh
if [[ ! $(podman machine ssh "echo test > /dev/null") ]]; then
    podman machine start
    ssh core@localhost -p 52090 -i ~/.ssh/podman-machine-default \
    -fL 12979:localhost:2979 \
    'podman system service --time=0 tcp:0.0.0.0:2979'
fi
```

