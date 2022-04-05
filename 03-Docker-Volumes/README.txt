```
  407  docker ps
  408  docker volume ls
  409  docker volume rm ef2f4a4b63bd1994795efd3a49794e97af63cb76c74fd93a4963c5073586b879
  410  docker volume ls
  411  docker volume create my-vol
  412  docker volume ls
  413  docker volume inspect my-vol
  414  ls -ltr "/var/lib/docker/volumes/my-vol/_data"
  415  docker run -it --name vol-test-1 --mount source=my-vol,target=/amit ubuntu:16.04
  416  docker ps
  417  docker inspect vol-test-1
  418  cat /var/lib/docker/volumes/my-vol/_data/hello.txt
  419  hostname
  420  hostname >> /var/lib/docker/volumes/my-vol/_data/hello.txt
  421  date >> /var/lib/docker/volumes/my-vol/_data/hello.txt
  422  docker ps
  423  docker attach vol-test-1
  424  docker ps
  425  docker ps -a
  426  docker rm vol-test-1
  427  docker ps -a
  428  docker volume ls
  429  cat /var/lib/docker/volumes/my-vol/_data/hello.txt
  430  docker run -it --name vol-test-2 --mount source=my-vol,target=/amit ubuntu:16.04
  431  docker ps
  432  docker ps -a
  433  docker run -it --name vol-test-3 -v /var/www/html/amit -v /var/log/amit -v /etc/amit  ubuntu:16.04
  434  docker ps
  435  docker inspect vol-test-3
  436  docker volume ls
  437  ls
  438  cd docker-k8s-vmware-04-April-2022/
  439  pwd
  440  cd ..
  441  docker run -it --name vol-test-4 -v /root/docker-k8s-vmware-04-April-2022:/myrepo  ubuntu:16.04
  442  docker run -it --name vol-test-5 -v /root/docker-k8s-vmware-04-April-2022:/myrepo:ro  ubuntu:16.04
  443  docker volume ls
  444  docker ps
  445  docker inspect vol-test-3
  446  docker inspect vol-test-3 | grep -B6 volume
  447  docker inspect vol-test-3 | grep -B6 "Mounts"
  448  docker inspect vol-test-3 | grep -B10 "Mounts"
  449  docker inspect vol-test-3 | grep -A10 "Mounts"
  450  docker inspect vol-test-5 | grep -A10 "Mounts"
  451  docker volume ls
  452  docker volume ls -q
  453  docker volume rm $(docker volume ls -q)
  454  docker kill $(docker ps -qa)
  455  docker rm $(docker ps -qa)
  456  docker volume rm $(docker volume ls -q)
  457  docker volume ls
```


```
 482  mkdir -p /var/www/html/
  483  ls
  484  docker run -d --name test-web-2 -v /var/www/html/:/var/www/html myapache:v2
  485  docker run -d --name test-web-3 -v /var/www/html/:/var/www/html myapache:v2
  486  docker inspect --format '{{.Name}}  {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  487  curl 172.17.0.3
  488  curl 172.17.0.4
  489  cd /var/www/html/
  490  ls
  491  docker ps
  492  vim index.html
  493  curl 172.17.0.4
  494  curl 172.17.0.3
  495  cd
  496  docker ps
  497  docker run -d --name test-web-4 --volumes-from test-web-2 myapache:v2
  498  docker run -d --name test-web-5 --volumes-from test-web-2 myapache:v2
  499  docker inspect --format '{{.Name}}  {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  500  curl 172.17.0.3
  501  curl 172.17.0.4
  502  curl 172.17.0.5
  503  curl 172.17.0.6
  504  vim /var/www/html/index.html
  505  curl 172.17.0.6
  506  curl 172.17.0.5
  507  curl 172.17.0.4
  508  curl 172.17.0.3

```
