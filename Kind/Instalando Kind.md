Referência
https://www.youtube.com/watch?v=1lx91nhzNe0


##Baixar Kind
```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/
```
**Obs**:Arquivos do Kind são binaŕios, sendo assim mover para pasta `/usr/local/bin/` para facilitar

##Criar Cluster
```
kind create cluster --name cluster01 --config kind-ingress.yaml
```

```
kind get clusters
```

```
kubectl get nodes
```

```
kind delete cluster
```




#iniciando ingress
kubectl apply -f teste-ingressprd.yaml