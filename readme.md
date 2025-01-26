# Grafana Stack for differnent environments

## Production 
The complete grafana stack with minIO as S3 storage. 

## Development 
This is the complete stack but with local file storage. 

## Remote 
This is only alloy that sends the data to a defined loki and tempo endpoint.


### Alloy config map

#### Create a new config map 
kubectl create configmap alloy-config --from-file=config.alloy=./values/config.alloy -n grafana-stack

#### Replace the config map
kubectl create configmap alloy-config --from-file=config.alloy=./values/config.alloy -n grafana-stack -o yaml --dry-run=client | kubectl replace -f -
