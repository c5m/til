# Docker Exec In Git Bash

To perform a `docker exec` command in git bash on windows we need to prefix the command with an extra `/`. As an example here is how to execute bash in a container

```sh
winpty docker exec -it <container-id> //bin/bash
```

