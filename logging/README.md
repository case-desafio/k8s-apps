
```
Executar primeiramente os comandos para criar o operator e 
na sequencia o arquivo kustomization.yml com os manifestos do fluentd, elasticsearch e kibana:

kubectl apply -f "operator.yml"

kustomize build . | kubectl apply -f -

usuário do kibana
elastic

obter senha do kibana
kubectl get secret quickstart-es-elastic-user -o=jsonpath='{.data.elastic}' | base64 --decode; echo
```