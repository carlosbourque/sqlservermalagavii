# GitHub Repository for the #sqlservermalagavii Meetup

## Demo 1: Creación de una base de datos en SQL Azure

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
az group create --name sqlmalagavii --location northeurope
```


The content of this repository is based on the following Azure documentation sites:

- [Azure SQL Database Documentation] (https://docs.microsoft.com/en-us/azure/sql-database/)