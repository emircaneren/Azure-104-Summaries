# List virtual machine associated network security groups
```shell
	az network nsg list \
	  --resource-group learn-****** \
	  --query '[].name' \
	  --output tsv

```

# List the associated rules of the "my-vmNSG" group.
```shell
	az network nsg rule list --resource-group learn-43fd6d79-814e-4112-897e-0a4cd91385bc 
--nsg-name my-vmNSG 
--query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' 
--output table

```
	