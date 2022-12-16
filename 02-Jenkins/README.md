# We need to setup a new virtual machine for our Jenkins Demo. 

## Create a resource group
```
az group create --name jenkins-rg --location eastus
```

## Create a virtual machine
```
az vm create --resource-group jenkins-rg  --name jenkinsVM --image "UbuntuLTS"  --admin-username azureuser    --admin-password Pass@word1234! --size="Standard_D2s_v3"
```

## Open port 80 for web traffic
```
az vm open-port --port 80 --resource-group jenkins-rg --name jenkinsVM
```
