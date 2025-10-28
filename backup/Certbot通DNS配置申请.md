
### 同步镜像
```shell
podman pull certbot/certbot
```

### 申请证书
```shell
podman run -it --rm --name certbot -v ./letsencrypt/:/etc/letsencrypt certbot/certbot certonly --manual --preferred-challenges dns -d 域名
```

### 按照提示配置TXT解析

### 查看证书

```shell
> ls ./letsencrypt/archive/域名/
> -rw-r--r-- 1 ubuntu ubuntu 2860 Jul 18 11:34 fullchain1.pem  #公钥
> -rw------- 1 ubuntu ubuntu  241 Nov  4  2024 privkey1.pem   #私钥
```