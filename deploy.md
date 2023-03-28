# dev vm
- [azureuser@20.51.151.168](https://portal.azure.com/#@guanxiyimetisthemis.onmicrosoft.com/resource/subscriptions/42c96549-22b8-4922-8538-ad92f11d2291/resourceGroups/rg-dev-01/providers/Microsoft.Compute/virtualMachines/jianfengzhu-dev-vm/overview)

# local docker build
```sh
sudo docker build -t feishu-chatgpt:latest .
sudo docker image list
sudo docker tag feishu-chatgpt:latest metisthemis.azurecr.io/feishu-chatgpt:latest
```
# push to Azure Container Register
- [Container registry](https://portal.azure.com/#@guanxiyimetisthemis.onmicrosoft.com/resource/subscriptions/42c96549-22b8-4922-8538-ad92f11d2291/resourceGroups/rg-dev-01/providers/Microsoft.ContainerRegistry/registries/metisthemis/overview)
- login `docker login metisthemis.azurecr.io`, user/pwd see [acr keys](https://portal.azure.com/#@guanxiyimetisthemis.onmicrosoft.com/resource/subscriptions/42c96549-22b8-4922-8538-ad92f11d2291/resourceGroups/rg-dev-01/providers/Microsoft.ContainerRegistry/registries/metisthemis/accessKey)
- push `docker push metisthemis.azurecr.io/feishu-chatgpt:latest`

# deploy as Azure Container Instance
- [current deployment](https://portal.azure.com/#@guanxiyimetisthemis.onmicrosoft.com/resource/subscriptions/42c96549-22b8-4922-8538-ad92f11d2291/resourceGroups/rg-dev-01/providers/Microsoft.ContainerInstance/containerGroups/feishu-chatgpt/overview)
- [how to deploy image as container instance](https://learn.microsoft.com/en-us/azure/container-instances/container-instances-quickstart-portal)

# lark config
see [readme.md]