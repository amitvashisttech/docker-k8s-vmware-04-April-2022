```
 387  kubectl apply -f 01-hello-deployment.yaml
  388  ls
  389  mv hello-svc.yaml 02-hello-svc.yaml
  390  ls
  391  vim 02-hello-svc.yaml
  392  cat 01-hello-deployment.yaml
  393  vim 02-hello-svc.yaml
  394  kubectl apply -f 02-hello-svc.yaml
  395  kubectl get svc
  396  kubectl get pods -o wide
  397  kubectl get pods --show-labels
  398  kubectl get pods -o wide
  399  kubectl get pods --show-labels
  400  kubectl describe svc helloworld-service
  401  cat 02-hello-svc.yaml
  402  cat 01-hello-deployment.yaml
  403  curl 172.31.0.101:31005
  404  curl 172.31.0.101:31001
  405  curl 172.31.0.102:31001
  406  ls
  407  kubectl  get svc
  408  mv mypyapp-svc.yaml 03-mypyapp-svc.yaml
  409  ls
  410  vim 03-mypyapp-svc.yaml
  411  cat 01-hello-deployment.yaml
  412  vim 03-mypyapp-svc.yaml
  413  kubectl apply -f 03-mypyapp-svc.yaml
  414  kubectl get svc
  415  vim 03-mypyapp-svc.yaml
  416  kubectl apply -f 03-mypyapp-svc.yaml
  417  kubectl  get pod,svc
  418  kubectl edit service/python-webapp-svc
  419  kubectl  get pod,svc
  420  vim 03-mypyapp-svc.yaml
  421  kubectl apply -f 03-mypyapp-svc.yaml
  422  kubectl  get pod,svc
  423  kubectl get pods -o wide
  428  kubectl  delete pod hello-nw
  429  kubectl run -it hello-nw-2 --image=amitvashist7/network-multitool  --restart=Never -- sh
  430  ls
  431  cd ..
  432  ls
  433  kubectl delete -f 07-Service/
```

```
# history
   0 curl 172.31.0.101:31001
   1 curl 172.31.0.102:31001
   2 curl 172.31.0.102:31007/info
   3 curl 10.107.104.128:31005
   4 curl 10.100.106.97:31007/info
   5 cat /etc/resolv.conf
   6 nslookup helloworld-service
   7 curl helloworld-service:31001
   8 curl helloworld-service:31005
   9 nslookup python-webapp-svc
  10 curl -vvv python-webapp-svc.default.svc.cluster.local:31007/info
  11 history
```
