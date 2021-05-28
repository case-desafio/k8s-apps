
```
Executar primeiramente os comandos para criar os operators e 
na sequencia o arquivo kustomization.yml com os manifestos do prometheus e grafana:

kubectl apply -f "prometheus/operator.yml"

curl -sL https://github.com/operator-framework/operator-lifecycle-manager/releases/download/v0.18.1/install.sh | bash -s v0.18.1
kubectl create -f https://operatorhub.io/install/grafana-operator.yml

kustomize build . | kubectl apply -f -
```