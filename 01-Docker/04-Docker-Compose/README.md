```
 526  cd 04-Docker-Compose/00-Setup/
  527  ls
  528  vim install-dockercompose.sh
  529  ls
  530  chmod +x install-dockercompose.sh
  531  ./install-dockercompose.sh
  532  ls
  533  cd
  534  docker-compose version
  535  ls
  536  cd docker-k8s-vmware-04-April-2022/
  537  ls
  538  cd 04-Docker-Compose/
  539  ls
  540  vim 01-Nginx
  541  mkdir 01-Nginx
  542  cd 01-Nginx/
  543  ls
  544  vim docker-compose.yaml
  545  ls
  546  docker images
  547  docker-compose up -d
  548  docker ps
  549  docker-compose ps
  550  docker-compose kill
  551  docker-compose ps
  552  docker-compose rm
  553  ls
  554  cat docker-compose.yaml
  555  ls
  556  cd ..
  557  ls
  558  cp -rf 01-Nginx 02-Multi-App
  559  ls
  560  cd 02-Multi-App/
  561  ls
  562  vim docker-compose.yaml
  563  ld
  564  ls
  565  docker-compose up -d
  566  docker-compose ps
  567  docker ps
  568  docker-compose ps
  569  docker-compose kill 02-multi-app_mypywebapp_1
  570  docker-compose kill mypywebapp
  571  docker-compose ps
  572  docker-compose up mypywebapp
  573  docker-compose up -d mypywebapp
  574  docker-compose ps
  575  ls
  576  vim docker-compose.yaml
  577  docker-compose up -d
  578  docker-compose ps
  579  docker-compose up -d
  580  vim docker-compose.yaml
  581* docker-compose up -
  582  docker-compose ps
```
