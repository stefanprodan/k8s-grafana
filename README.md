# k8s-grafana

Depends on:
 * Prometheus 
 * Kubelet cAdvisor metrics
 * Kube state metrics
 * Node Exporter metrics

Prometheus operator setup:

```bash
helm upgrade --install --wait prom \
 --namespace default \
 --set service.type=LoadBalancer \
 --set user=admin \
 --set password=admin \
 --set url=http://prometheus:9090 \
 ./chart/grafana
```

Weave Cloud setup:

```bash
helm upgrade --install --wait weave \
 --namespace weave \
 --set service.type=LoadBalancer \
 --set user=admin \
 --set password=admin \
 --set token=WEAVE-TOKEN \
 ./chart/grafana
```
