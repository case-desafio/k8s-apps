
```
Executar o comando abaixo para criar os recursos das aplicações:

kustomize build . | kubectl apply -f -

Comandos para retornar o host e porta do ingress para acessar as aplicações
export INGRESS_HOST=$(kubectl -n istio-system get service istio-ingressgateway -o jsonpath='{.status.loadBalancer.ingress[0].ip}')
export INGRESS_PORT=$(kubectl -n istio-system get service istio-ingressgateway -o jsonpath='{.spec.ports[?(@.name=="http2")].port}')

echo $INGRESS_HOST
echo $INGRESS_PORT
```