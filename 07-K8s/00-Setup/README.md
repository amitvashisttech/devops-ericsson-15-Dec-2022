# Setup AKS Cluster


## Create a resource group
```
az group create --name myaksrg --location eastus
```

## Create AKS cluster
```
az aks create -g myaksrg -n myAKSCluster --enable-managed-identity --node-count 2 --enable-addons monitoring --enable-msi-auth-for-monitoring  --generate-ssh-keys
```

## Connect to the cluster
```
az aks get-credentials --resource-group myaksrg --name myAKSCluster
``` 

## Check the No. of Nodes into the Cluster
```
kubectl get nodes
```

```
$ kubectl get nodes 
NAME                                STATUS   ROLES   AGE     VERSION
aks-nodepool1-17628576-vmss000000   Ready    agent   4m19s   v1.24.6
aks-nodepool1-17628576-vmss000001   Ready    agent   4m30s   v1.24.6
$ 

```
