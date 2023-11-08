# Create A Linux Virtual Machine on CLI


```shell
az vm create \
  --resource-group learn-****** \
  --name my-vm \
  --public-ip-sku Standard \
  --image Ubuntu2204 \
  --admin-username azureuser \
  --generate-ssh-keys
```


