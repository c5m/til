# Docker CMD vs. ENTRYPOINT



The difference between `CMD`  and `ENTRYPOINT` is that `CMD` can be overwritten when using `docker run`.
But 	`ENTRYPOINT` and `CMD` can be used in combination to set defaulty arguments which can be overwritten. 

Example

```dockerfile
FROM ubuntu:latest
ENTRYPOINT ["echo" "Hello"]
CMD ["world"]
```

