Documentação de Referência:
https://docs.microsoft.com/en-us/azure/aks/ingress-tls?tabs=azure-cli


kubectl create namespace ingress-basic \
--namespace ingress-basic \
ou
--namespace ingress-basic --create-namespace \

--set controller.replicaCount=2 \
--set controller.nodeSelector."kubernetes\.io/os"=linux \
--set defaultBackend.nodeSelector."kubernetes\.io/os"=linux \
--set controller.admissionWebhooks.patch.nodeSelector."kubernetes\.io/os"=linux 

