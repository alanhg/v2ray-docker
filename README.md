# v2ray-docker
v2ray deploy by docker

## GetStarted

Notice: `CentOS 7 x64`

1. add dns a record vps ip on site
2. deploy ss service
   ```sh
   yum install -y unzip
   curl -LJO curl -LJO https://github.com/alanhg/v2ray-docker/archive/refs/tags/own-use.zip
   unzip v2ray-docker-own-use.zip
   
   # replace ray.alanhe.me,qianghe421@gmail.com with your domain name,email, file: init-letsencrypt.sh, nginx/conf.d/default.conf
   
   
   # following setting is optional
   # setting your clients id, file: v2ray/config.json 
   # setting ws path, file: nginx/conf.d/default.conf, nginx/conf.d/default.conf
   
   # execute the following command
   chmod +x ./*.sh
   ./init-v2ray.sh

   # setting timezone 
   timedatectl set-timezone Asia/Shanghai
   
   ```
 
## Speed Test 

```bash
# abroad
$ wget -qO- bench.sh | bash

# home
$ wget -qO- git.io/superbench.sh | bash
```


## Client Config

### Surge
```
[Proxy]
proxy1 = vmess, ray.me, 443, username=3fc6edef-eae9-400a-be45-220ff5aa982e, ws=true, ws-path=/helloworld, tls=true
```

### Clash
```
proxies:
  - 
    name: proxy1
    type: vmess
    server: ray.me
    port: 443
    uuid: 3fc6edef-eae9-400a-be45-220ff5aa982e
    alterId: 64
    cipher: auto
    tls: true
    skip-cert-verify: false
    network: ws
    ws-path: /helloworld
```
