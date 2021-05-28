
```
Executar primeiramente os comandos para criar o operator e 
na sequencia o arquivo kustomization.yml com os manifestos do fluentd, elasticsearch e kibana:

kubectl apply -f operator.yml

kustomize build . | kubectl apply -f -

para acessar o kibana
kubectl port-forward service/quickstart-kb-http -n elastic-system 5601
https://localhost:5601

usuário do kibana
elastic

obter senha do kibana
kubectl -n elastic-system get secret quickstart-es-elastic-user -o=jsonpath='{.data.elastic}' | base64 --decode; echo
```