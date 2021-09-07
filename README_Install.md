Overview


```
git clone https://github.com/BrianMcMaster/opencanary
sudo docker build -t opencanary -f Dockerfile.stable .
sudo docker images
sudo docker run -it opencanary /bin/bash
opencanaryd --copyconfig
grep enable /etc/opencanaryd/opencanary.conf
exit
sudo docker ps -l
sudo docker commit 67b16dfa404c opencanary:latest
sudo docker run -p 21:21 -it opencanary /bin/bash
opencanaryd --start
tail -f /var/tmp/opencanary.log
ftp <ip address>
```