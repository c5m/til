# Find Open Ports

To find ports in `LISTEN` mode do

on `osx`

```shell
sudo lsof -i -P | grep -i "listen"
```

or without `sudo` 

```shell
lsof -PiTCP -sTCP:LISTEN
```



on `Linux`

```shell
netstat -aep | grep ':\*'
```

