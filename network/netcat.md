# Check if port is open

```shell
nc -zv $host $port
```

## Example

```shell
$ nc -zv s3.us-west-2.amazonaws.com 443
Connection to s3.us-west-2.amazonaws.com port 443 [tcp/https] succeeded!
```

# Check which process bind to local port

```shell
$ sudo lsof -n -i :8000
COMMAND   PID       USER   FD   TYPE            DEVICE SIZE/OFF NODE NAME
Python  68928 stevezhang    5u  IPv6 0x5b28893dbafee15      0t0  TCP *:irdmi (LISTEN)
```