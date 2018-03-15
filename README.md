# k8s-grafana

Weave Cloud setup:

```bash
# set your Weave Cloud token with
sed -i .bak -e 's/WEAVE-TOKEN/YOUR-TOKEN/g' weave-cloud/datasources-cfg.yaml
```

Deploy Grafana in weave namespace:

```bash
kubectl -n weave apply -f ./weave-cloud/
```

Access Grafana with user/pass `admin/admin` on the NodePort:

```bash
kubectl -n weave get svc --selector=component=grafana
NAME                   TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)          AGE
grafana                NodePort    10.59.250.45   <none>        3000:30843/TCP   9m
```

