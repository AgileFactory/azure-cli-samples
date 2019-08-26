* Create a firewall at postgresql level
```
az postgres server firewall-rule create --resource-group myresourcegroup --server mydemoserver --name AllowMyIP --start-ip-address 192.168.0.1 --end-ip-address 192.168.0.1
```


* List databases from an instances
* Create a firewall at postgresql level
```
az postgres db list  -g myresourcegroup -s irgdevpostgres
mydemoserver --name AllowMyIP --start-ip-address 192.168.0.1 --end-ip-address 192.168.0.1
```


* Delete database
```
az postgres db delete  -g <resource_group > -s <server_name > -n <database_name>
```
