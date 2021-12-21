Documentação de Referência:
https://docs.microsoft.com/en-us/azure/aks/ingress-tls?tabs=azure-cli

https://docs.oracle.com/pt-br/iaas/Content/ContEng/Tasks/contengsettingupingresscontroller.htm

https://kubernetes.io/docs/concepts/services-networking/ingress/

#dns
https://www.valuehost.com.br/blog/configurar-dns-no-linux/

https://kubernetes.io/docs/concepts/services-networking/ingress/#tls

https://www.ti-enxame.com/pt/ssl/o-kubernetes-nginx-ingress-controller-nao-obtem-certificados-tls/833932524/


#listar varios recursos namespace
kubectl get deploy,pod,rs,svc,ing -n test-ingress

#listar ingress de uma namespace
kubectl get ingress -n gdt-dev


Criar certificado
kubectl create secret tls tls-secret --key tls.key --cert tls.crt

kubectl create secret tls tls-secret \
    --namespace gdt-prd \
    --key tls.key \
    --cert tls.crt


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

