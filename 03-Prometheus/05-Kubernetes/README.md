```

https://istio.io/latest/docs/setup/getting-started/#download

curl -L https://istio.io/downloadIstio | sh -


kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.11/samples/bookinfo/platform/kube/bookinfo.yaml

kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.11/samples/addons/prometheus.yaml

kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.11/samples/addons/grafana.yaml

https://istio.io/latest/docs/ops/integrations/grafana/#option-1-quick-start


Trafic Genrater:
================>
 for i in $(seq 1 100); do curl -s -o /dev/null "http://172.31.0.101:30321/productpage"; done

```
