```
  127  mkdir 04-Replicas-Cantroller/
  128  ls
  129  cd 04-Replicas-Cantroller/
  130  ls
  131  vim hello-rc.yaml
  132  ls
  133  kubectl  get pods
  134  kubectl  apply -f hello-rc.yaml
  135  kubectl  api-resources
  136  kubectl  get rc
  137  kubectl  get pods
  138  kubectl  delete pod hello-k8s helloworld-controller-cwthv
  139  kubectl  get pods
  140  kubectl  delete pod --all
  141  kubectl  get pods
  142  kubectl scale --replicas=5 rc helloworld-controller
  143  kubectl  get pods
  144  kubectl scale --replicas=1 rc helloworld-controller
  145  kubectl  get pods
  146  kubectl  get rc
  147  ls
  148  kubectl  delete -f hello-rc.yaml
  149  kubectl  get rc
  150  kubectl  get pods
```
