kubectl create configmap alloy-config --from-file=config.alloy=./values/config.alloy -n grafana-stack

kubectl get configmap alloy-config -n grafana-stack -o yaml

kubectl create configmap alloy-config --from-file=config.alloy=./values/config.alloy -n grafana-stack -o yaml --dry-run=client | kubectl replace -f -
