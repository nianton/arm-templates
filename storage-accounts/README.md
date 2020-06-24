# Multiple Storage Acccounts

[![Deploy To Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnianton%2Farm-templates%2Fmaster%2Fstorage-accounts%2Fazuredeploy.json)


This template deploys a series of **Storage Accounts** in a sequential fashion. You may configure the following in the process:
* The count of the storage accounts to be created (e.g. with 'snet' as prefix, the resulting subnets will be named: 'snet-00', 'snet-01' and so on)
* Prefix of the storage accounts to be created (e.g. for three storage accounts and prefix "smyappdatadev", the storage accounts created will be named "smyappdatadev000", "smyappdatadev001" and "smyappdatadev002"
* Storage account type (defaults to Standard LRS)
* Whether the storage accounts will only support Https only -boolean, defaults to **true**
* Additional storage accounts properties for configure the storage accounts -JSON object, [reference](https://docs.microsoft.com/en-us/azure/templates/microsoft.storage/2019-06-01/storageaccounts#storageaccountpropertiescreateparameters-object)
* The set of tags to be created -JSON object, e.g. { "environment": "dev", "project": "megastore" }

The resulting storage accounts 5 with prefix of "smyappdatadev" and default parameters will be:

![alt text](https://raw.githubusercontent.com/nianton/arm-templates/master/.assets/multiple-subnets-diagram.png "Virtual Network topology result")


If you are new to template deployment, see:

[Azure Resource Manager documentation](https://docs.microsoft.com/azure/azure-resource-manager/)
