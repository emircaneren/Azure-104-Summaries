# Getting Virtual Machine IP and saving the result in Bash as a TSV
```shell
IPADDRESS="$(az vm list-ip-addresses \
  --resource-group learn-************** \
  --name my-vm \
  --query "[].virtualMachine.network.publicIpAddresses[*].ipAddress" \
  --output tsv)"
```