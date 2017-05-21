
### Using Portal
Open Azure portal and follow the steps to create a new SQL Database. Also see how easy would be to create a SQL Server (IaaS) in a VM environment.

### Using Azure CLI
Install Azure CLI in Windows, Linux or MacOS.

#### 1.- Log in to Azure

Log in to your Azure subscription with the [az login](https://docs.microsoft.com/en-us/azure/cli/azure/#login) command and follow the on-screen directions.

```azurecli
az login
```

#### 2.- Create a resource group

Let's create a resource group for our tests in Azure. The resource group will be called 'sqlmalagavii'

```azurecli
az group create --name sqlmalagavii-rg --location northeurope
```

#### 3.- Create a server

We create a server where the database will be hosted

```azurecli
az sql server create --name sqlmalagavii-sql2 --resource-group sqlmalagavii-rg --location northeurope  --admin-user Carlos --admin-password ChangeYourAdminPassword1
```

#### 4.- Set up the firewall rule

```azurecli
az sql server firewall-rule create --resource-group sqlmalagavii-rg --server sqlmalagavii-sql2 -n AllowYourIp --start-ip-address [yourIP]  --end-ip-address [yourIP]
```

#### 5.- Add the database

Then, we add the database to the server we just created

```azurecli
az sql db create --resource-group sqlmalagavii-rg --server sqlmalagavii-sql2 --name sqlmalagavii-db --sample-name AdventureWorksLT --service-objective S0
```

#### 6.- Remove the resource group

```azurecli
az group delete --name sqlmalagavii-rg
```