Documentação de Referência:
https://docs.microsoft.com/en-us/azure/aks/ingress-tls?tabs=azure-cli

https://docs.oracle.com/pt-br/iaas/Content/ContEng/Tasks/contengsettingupingresscontroller.htm


`kubectl delete namespace <nome-namespace>`

k8s.gcr.io/echoserver:1.4 > porta:8080


kubectl create namespace ingress-basic \
--namespace ingress-basic \
ou
--namespace ingress-basic --create-namespace \

--set controller.replicaCount=2 \
--set controller.nodeSelector."kubernetes\.io/os"=linux \
--set defaultBackend.nodeSelector."kubernetes\.io/os"=linux \
--set controller.admissionWebhooks.patch.nodeSelector."kubernetes\.io/os"=linux 

