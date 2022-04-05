# Creating out First App

## Check the health of Cluster
```
kubectl get nodes 
```

## Deploy Nginx App
```
kubectl run hello-k8s --image=nginx --port=80
```

## Check the status of PODs 
```  
kubectl get pods 
kubectl describe pods hello-k8s
```

## Let's Deploy our newly built PythonWeb App.
```
kubectl run mypythonwebapp --image=amitvashist7/mypython-webapp-vmware-05-april-2022:v1 --port=8080
```
```
kubectl get pods
NAME             READY   STATUS    RESTARTS   AGE
hello-k8s        1/1     Running   0          6m22s
mypythonwebapp   1/1     Running   0          4m58s
```


## Let's Remove the POD's 
``` 
kubectl delete pod hello-k8s
kubectl get pods -o wide
kubectl delete pod --all
```


Note Point : In Case you are getting imagepull error stating that you have reached to max limit of downloads, then apply the following solution. 

# Docker login
```
docker login
ls /root/.docker/config.js
```

# Create a Secret in K8s for Docker Registry
```
kubectl create secret generic regcred --from-file=.dockerconfigjson=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson

kubectl get secrets
```

# Now you can source your secret in POD Deployment file & Good to go. 
```
kubectl run hello-k8s --image=nginx --port=80 -o yaml --dry-run > nginx-pod.yaml
```

## Update the Pull Defination in Yaml File 
```
      imagePullSecrets:
      - name: regcred
```

## Now deploy the nginx POD.
```
kubectl apply -f nginx-pod.yaml
```

