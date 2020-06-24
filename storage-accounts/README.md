# Multiple Storage Acccounts

[![Deploy To Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnianton%2Farm-templates%2Fmaster%2Fstorage-accounts%2Fazuredeploy.json)


This template deploys a series of **Storage Accounts** in a sequential fashion. You may configure the following in the process:
* Prefix of the storage accounts to be created 
* The count of the storage accounts to be created (e.g. for three storage accounts and prefix "smyappdatadev", the resulting storage accounts  will be named "smyappdatadev000", "smyappdatadev001" and "smyappdatadev002")
* Storage account type (defaults to Standard LRS)
* Whether the storage accounts will only support Https only -boolean, defaults to **true**
* Additional storage accounts properties for configure the storage accounts -JSON object, [reference](https://docs.microsoft.com/en-us/azure/templates/microsoft.storage/2019-06-01/storageaccounts#storageaccountpropertiescreateparameters-object)
* The set of tags to be created -JSON object, e.g. { "environment": "dev", "project": "megastore" }

The resulting storage accounts 3 with prefix of "smyappdatadev" and default parameters will be:

![alt text](https://raw.githubusercontent.com/nianton/arm-templates/master/.assets/multiple-subnets-diagram.png "Virtual Network topology result")

and the output of the template will be the following:

```json 
{
  "storageEndpoints": [
    {
      "id": "Microsoft.Storage/storageAccounts/smyappdatadev000",
      "blobEndpoint": "https://smyappdatadev000.blob.core.windows.net/",
      "connectionString": "DefaultEndpointsProtocol=https;AccountName=smyappdatadev000;AccountKey=[ACCOUNT_KEY_VALUE]"
    },
    {
      "id": "Microsoft.Storage/storageAccounts/smyappdatadev001",
      "blobEndpoint": "https://smyappdatadev001.blob.core.windows.net/",
      "connectionString": "DefaultEndpointsProtocol=https;AccountName=smyappdatadev001;AccountKey=[ACCOUNT_KEY_VALUE]"
    },
    {
      "id": "Microsoft.Storage/storageAccounts/smyappdatadev002",
      "blobEndpoint": "https://smyappdatadev002.blob.core.windows.net/",
      "connectionString": "DefaultEndpointsProtocol=https;AccountName=smyappdatadev002;AccountKey=[ACCOUNT_KEY_VALUE]"
    }
  ]
}
```

If you are new to template deployment, see:

[Azure Resource Manager documentation](https://docs.microsoft.com/azure/azure-resource-manager/)
