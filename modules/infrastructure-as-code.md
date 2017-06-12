# Infrastructure as code #

## Azure CLI 2.0 ##

https://docs.microsoft.com/en-us/cli/azure/install-az-cli2


## Azure Template ##

- https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-kv-deploy-vm-with-secret
- https://blog.siliconvalve.com/2015/11/30/no-more-plaintext-passwords-using-azure-key-vault-with-azure-resource-manager/

### How to deploy with Azure Template - Powershell ###

	PS C:\Users\runemy\git\test-azurerm-vs-code> .\deploy.ps1 -subscriptionId c6179f90-6865-40b7-9af8-d9bfc58049a3 -resourceGroupName vscode -resourceGroupLocation westeurope -deploymentName vscode -parametersFilePath .\testparam.json

### Links ###

- https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-template-best-practices
- https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-keyvault-parameter
- https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-template-walkthrough

## Terraform ##

- https://github.com/hashicorp/terraform
- https://www.terraform.io/
- https://blogs.msdn.microsoft.com/eugene/2016/11/03/creating-azure-resources-with-terraform/
- https://doics.co/2015/08/13/using-terraform-with-microsoft-azure/
- http://www.thehyperadvisor.com/cloud-computing/terraform-your-azure-infrastructure/'
- https://pgroene.wordpress.com/2016/06/14/getting-started-with-terraform-on-windows-and-azure/
- http://toddysm.com/2016/12/08/how-to-configure-terraform-to-work-with-azure-resource-manager/
- http://qiita.com/TsuyoshiUshio@github/items/60df866ffeff10c0b6e1
- https://marketplace.visualstudio.com/items?itemName=mauve.terraform


`The “plan” Terraform command, looks at the resources defined in the scripts, compares them to the state information saved by Terraform and then outputs planned execution without actually creating resources in Azure.`

Create client_id and client_secret

	az login
	az account set --subscription="c6179f90-6865-40b7-9af8-d9bfc58049a3" 
	az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/c6179f90-6865-40b7-9af8-d9bfc58049a3"
