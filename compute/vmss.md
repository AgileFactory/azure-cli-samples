# Project Az (Python-based Azure CLI) Samples - Compute Service

Compute Topics:
* [General](compute.md)
* [Managing ScaleSets](vmss.md)
* [Managing Availability Sets](availability-set.md)
* [Managing Azure Container Services](container-service.md)

# (Optional) Create a new resource group
When trying new things out, consider creating a new resource group to experiment with:
> Many creation commands will use the resource group's location as a default value.
```
az group create -l westus -n MyRG
```

Here are some useful commands that may help you on your journey
* Delete this RG `az group delete -n MyRG`
* Export to ARM template `az group export -n MyRG > ./MyTemplate.json`

# Managing Azure virtual machine scale sets (VMSS)

create a new virtual machine scale set
```
az vmss show create -g mygroup -n MyScaleSet --image opensuse --instance-count 3
```

get a list of all scale sets
```
az vmss show list -g MyGroup
```

get a list of all VMs in a scale set
```
az vmss show list-instances -g MyGroup -n MyScaleSet
```

show a VM in a scale set
```
az vmss show --resource-group DEVRG --name myVMSS --instance-id 0
```

stop two vms
```
az vmss show stop -g MyGroup -n MyScaleSet --instance-ids 0 2
```
stop all vms in a scale set
```
az vmss show stop -g MyGroup -n MyScaleSet
```

az vmss get-instance-view \
    --resource-group DEVRG\
    --name myVMSS \
    --instance-id 0



 List ip adress from VMSS
```
 az vmss list-ip-adresses  -n myVMSS --resource-group iasearch-fraud-lab-rg --subscription <subscription>
 ```


 List nic car from VMSS
```
 az vmss nic list  --vmss-name  <VMSS NAME>  --resource-group <RESOURCE GROUP> --subscription <subscription>
 ```
