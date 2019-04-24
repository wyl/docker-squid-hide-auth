
docker-squid-hide-auth
=====================

使用Dockerfile 创建一个简单的需要认证的squid http proxy。

The user must specify authentication credentials via the following environment variables:

```
SQUID_PORT=3128
SQUID_CONFIG_FILE=squid.base.conf
SQUID_USERNAME=name
SQUID_PASSWORD=password
```

Environment variables
---------------------
* SQUID_PORT
* SQUID_CONFIG_FILE
* SQUID_USERNAME
* SQUID_PASSWORD

Ports
-----

* 3128

Volumes
-------

* `/var/log/squid`
  
  Ideas for Improvement
=====================
* Output logs to stdout.
* 

Test
-------

curl -x http://user:password@localhost:3128 http://ipinfo.io/ip -v


