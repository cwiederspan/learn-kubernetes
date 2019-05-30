# Use the Azure CLI to Create a Simple AKS Cluster

```bash
RG_NAME=my-kubernetes-20190529
LOCATION=westus2
VERSION=1.14.0

az group create --name $RG_NAME --location $LOCATION

az aks create --resource-group $RG_NAME \
    --name $RG_NAME \
    --location $LOCATION \
    --enable-addons monitoring \
    --kubernetes-version $VERSION \
    --generate-ssh-keys
```