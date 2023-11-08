# Creating the network security rule.
A network secure rule will be created that allows incoming traffic over port 80 (HTTP).

```shell
		az network nsg rule create \
		  --resource-group learn-43fd6d79-814e-4112-897e-0a4cd91385bc \
		  --nsg-name my-vmNSG \
		  --name allow-http \
		  --protocol tcp \
		  --priority 100 \
		  --destination-port-range 80 \
		  --access Allow \
		  --output table

```