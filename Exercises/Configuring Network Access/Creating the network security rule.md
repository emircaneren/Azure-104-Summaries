# Creating the network security rule.
A network secure rule will be created that allows incoming traffic over port 80 (HTTP).

```shell
		az network nsg rule create \
		  --resource-group learn-00000000 \
		  --nsg-name my-vmNSG \
		  --name allow-http \
		  --protocol tcp \
		  --priority 100 \
		  --destination-port-range 80 \
		  --access Allow \
		  --output table

```

# Verify the configuration

```shell
	az network nsg rule list 
	--resource-group learn-00000000 
	--nsg-name my-vmNSG 
	--query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' 
	--output table
```