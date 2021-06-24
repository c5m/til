# Docker Remote Debug



## Java



Set the `JAVA_TOOL_OPTIONS` to the following string

```
-agentlib:jdwp=transport=dt_socket,server=y,suspend=y,address=*:5005
```

in Docker this can be set in the `Dockerfile` using the `ENV` keyword or on the CLI like 
(remember to also expose ports)

```sh
docker run -it -p 5005:5005 --env \
JAVA_TOOL_OPTIONS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=y,address=*:5005" \
<image>
```



```sh
-Xrunjdwp=transport=dt_socket,server=y,suspend=y,address=*:5005
```



If we get the error `No java installations was detected.` it might be because [sbt-launch-lib.bash](https://github.com/sbt/sbt-launcher-package/blob/6935bee2c7b6123f93ad4e96db11acf315671929/src/universal/bin/sbt-launch-lib.bash#L276) is unable process the `JAVA_TOOL_OPTIONS`.

