
```
Executar primeiramente os comandos para criar o operator e 
na sequencia o arquivo kustomization.yml com os manifestos do fluentd, elasticsearch e kibana:

kubectl apply -f "operator.yml"

kustomize build . | kubectl apply -f -
```