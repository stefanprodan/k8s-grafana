# k8s-grafana

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
