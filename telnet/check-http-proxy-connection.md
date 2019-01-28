# Check HTTP Proxy Connection with Telnet

```sh
telnet <proxy-address>
GET http://google.com HTTP/1.1
Proxy-Connection: Keep-Alive
Connection: Keep-Alive
```