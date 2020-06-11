# Virtual Network with multiple subnets

[![Deploy To Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnianton%2Farm-templates%2Fmaster%2Fmultiple-subnets%2Fazuredeploy.json)


This template deploys a **Virtual Network** with multiple subnets in a configurable fashion. You may configure the following in the process:
* Number of subnets
* Prefix of the subnet names (e.g. with 'snet' as prefix, the resulting subnets will be named: 'snet-00', 'snet-01' and so on)
* Subnet address space template (e.g. with '10.0.x.0/24' the resulting subnets will have adress spaces like '10.0.0.0/24', '10.0.1.0/24' and so on)

The resulting virtual network for 5 subnets with the default parameters is like the following:

![alt text](https://raw.githubusercontent.com/nianton/arm-templates/master/.assets/multiple-subnets-diagram.png "Virtual Network topology result")


If you are new to template deployment, see:

[Azure Resource Manager documentation](https://docs.microsoft.com/azure/azure-resource-manager/)
