# Kubernetes

```bash
k8s-login () {
	AKS_RESOURCE_GROUP=$(az aks list --subscription "${1}" --query "[?name=='${2}'] | [0].resourceGroup" --output tsv) 
	az aks get-credentials --subscription "${1}" --name "${2}" --resource-group "${AKS_RESOURCE_GROUP}" --file "~/.kube/config${3}"
	kubectl config set-context --current
}
```

Example
```bash
k8s-login maps-autostream-sandbox euw-aks-01 -sandbox
```
