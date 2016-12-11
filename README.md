# Azure-POC-Template

This repository contains a simple Azure template for demoing a CloudShell Azure deployment. The deployment architecuture is intended for demo/POC purposes and is not suitable for production environments.

Click the button below to deploy this template to your Azure account:

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FQualiSystems%2FAzure-POC-Template%2Fmaster%2Fmain_template.json)

## Deployment Architecture

The following diagram descibes the deployment topology.  

![Deployment Architecture](https://github.com/QualiSystems/Azure-POC-Template/raw/master/POC_CloudShell_AZURE_ARCH.png)

As seen in the above diagram this template will create the following elements in Azure:

1. CloudShell Mgmnt VNET
2. CloudShell Mgmnt Subnet
3. CloudShell Mgmnt Storage
4. CloudShell Mgmnt Resource Group
4. CloudShell Mgmnt Security Group
5. Windows VM (default A-3)for the following products (installed separately): CloudShell Portal, Quali server, Execution Server, CloudShell DB
6. Linux VM (default A-2) for the following product: QualiX
5. CloudShell Sandboxes VNET
6. Peering between the CloudShell Sandboxes VNET and the CloudShell Mgmnt VNET

Note that additional VMs may be dynamically allocated for each sandbox.
