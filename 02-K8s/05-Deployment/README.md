```
248  mkdir 05-Deployment
  249  ls
  250  cd 05-Deployment/
  251  ls
  252  vi helloworld.yaml
  253  kubectl apply -f helloworld.yaml
  254  kubectl  get deploy
  255  kubectl  get rs
  256  kubectl  get pods
  257  kubectl scale --replicas=2 deploy helloworld-deployment
  258  kubectl get pods
  259  kubectl expose deploy helloworld-deployment --type=NodePort
  260  kubectl get svc
  261  kubectl get pods -o wide
  262  kubectl  get deploy
  263  kubectl  describe deploy helloworld-deployment
  264  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2
  265  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3
  266  kubectl  get deploy
  267  kubectl describe deploy helloworld-deployment
  268  kubectl  get rs
  269  kubectl  describe rs helloworld-deployment-58857f8b94
  270  kubectl  get rs
  271  kubectl  describe rs helloworld-deployment-868844986
  272  kubectl  describe rs helloworld-deployment-6dc5c45bf7
  273  cd
  274  kubectl rollout history deploy helloworld-deployment
  275  kubectl rollout history deploy helloworld-deployment --revision=1
  276  kubectl rollout history deploy helloworld-deployment --revision=2
  277  kubectl rollout history deploy helloworld-deployment --revision=3
  278  kubectl scale --replicas=10 deploy helloworld-deployment
  279  kubectl rollout status  deploy helloworld-deployment
  280  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4
  281  kubectl rollout status  deploy helloworld-deployment
  282  kubectl rollout history deploy helloworld-deployment
  283  kubectl rollout undo deploy helloworld-deployment
  284  kubectl scale --replicas=2 deploy helloworld-deployment
  285  kubectl rollout history deploy helloworld-deployment
  286  kubectl rollout undo deploy helloworld-deployment
  287  kubectl rollout history deploy helloworld-deployment
  288  kubectl rollout undo deploy helloworld-deployment --to-revision=1
  289  kubectl rollout history deploy helloworld-deployment
  290  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web --record
  291  kubectl rollout history deploy helloworld-deployment
  292  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  293  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  294  kubectl set image deploy helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  295  kubectl rollout history deploy helloworld-deployment
  296  kubectl rollout undo deploy helloworld-deployment
  297  kubectl rollout history deploy helloworld-deployment
  298  kubectl  get deploy
  299  kubectl  describe deploy
  300  kubectl  get rs
  301  kubectl  describe rs helloworld-deployment-6dc5c45bf7
  302* kubectl  ge
  303  kubectl  describe rs helloworld-deployment-868844986
  304  kubectl  describe deploy
  305  ls
  306  cd docker-k8s-vmware-04-April-2022/
  307  ls
  308  cd 02-K8s/
  309  ls
  310  cd 05-Deployment/
  311  ls
  312  kubectl  delete -f helloworld.yaml
```

```
  313  vim helloworld-v2.yaml
  314  kubectl  apply -f helloworld-v2.yaml
  315  kubectl set image deploy helloworld-2-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  316  kubectl set image deploy helloworld-2-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  317  kubectl  delete -f helloworld-v2.yaml
```

```
  318  vim helloworld-v3.yaml
  319  kubectl  apply -f helloworld-v3.yaml
  320  kubectl set image deploy helloworld-3-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  321  kubectl set image deploy helloworld-3-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  322  kubectl  delete  -f helloworld-v3.yaml
```
