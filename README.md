# v2ray-docker
v2ray deploy by docker

## GetStarted

Notice: `CentOS 7 x64`

1. add dns a record vps ip on site
2. deploy ss service
    - yum install -y unzip
    - curl -LJO https://github.com/alanhg/v2ray-docker/archive/own-use.zip
    - unzip v2ray-docker-own-use.zip
    - replace ray.alanhe.me,qianghe421@gmail.com with your domain name,email
    - setting your clients id on v2ray/config.json  
    - execute the following command

	```bash
	$ chmod +x ./*.sh
	$ ./init-v2ray.sh
	
		
	# Pay attention to time zone
	$ timedatectl set-timezone Asia/Shanghai
	
	```
 
## Speed Test 

```bash
# abroad
$ wget -qO- bench.sh | bash

# home
$ wget -qO- git.io/superbench.sh | bash
```
