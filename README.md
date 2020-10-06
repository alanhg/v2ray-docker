# v2ray-docker
v2ray deploy by docker

## GetStarted

Notice: `CentOS 7 x64`

1. replace ray.me,xxx@gmail.com with your domain name,email
2. setting your clients id on v2ray/config.json  
3. add dns a record vps ip on site
4. deploy ss service
    - yum install -y unzip
    - curl -LJO https://github.com/alanhg/v2ray-docker/archive/own-use.zip
    - unzip v2ray-docker-own-use.zip
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
