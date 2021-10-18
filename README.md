# grafana-tempo
POC for grafana tempo

## Minikube Setup
[Already done here](https://github.com/shreyasgune/grafana-tempo.git)

## Steps
```
helm repo add grafana https://grafana.github.io/helm-charts

helm upgrade --install tempo grafana/tempo

helm upgrade -f microservices-grafana-values.yaml --install grafana grafana/grafana

kubectl create -f microservices-extras.yaml

kubectl logs synthetic-load-generator-####-###

kubectl port-forward deployments/grafana 3000

http://localhost:3000/explore
```

