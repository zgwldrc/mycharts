## opensearch

## etcd

helm repo add bitnami https://charts.bitnami.com/bitnami
helm fetch --untar bitnami/etcd

etcdctl --write-out=table --endpoints=etcd.local.com endpoint status
etcdctl --endpoints=etcd.local.com --user=root:90CjPHPRlxw= endpoint health
etcdctl --write-out=table --endpoints=etcd.local.com member list

## grafana

- import dashboards at line:652 under filed dashboards

    helm -n devops upgrade -i grafana system/devops/grafana
