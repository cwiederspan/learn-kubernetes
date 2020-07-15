# Use the Azure CLI to Create an AKS Cluster

You can use the Azure CLI to [create an AKS Cluster](https://docs.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-create).

```bash

# Get the versions of AKS that are available for a region
az aks get-versions -l westus2 -o table

# Setup some variables to use
RG_NAME=my-kubernetes-20200715
LOCATION=westus2
VERSION=1.17.7

# Create a resource group for the cluster
az group create --name $RG_NAME --location $LOCATION

# Create the Kubernetes cluster
az aks create \
    --resource-group $RG_NAME \
    --name $RG_NAME \
    --location $LOCATION \
    --enable-addons monitoring \
    --kubernetes-version $VERSION \
    --node-count 2

```
