# Installing the Azure Az Module for PowerShell Core
## Introduction: 

The Az module in PowerShell Core is necessary for managing Azure resources. In this hands-on lab, we will show how to install the Az module and perform some basic commands for managing resources in Azure.

- Log in to the VM
- Open a terminal session.
- Log in to the virtual machine via SSH using the credentials   provided on the lab page:
```
    ssh cloud_user@<PUBLIC_IP_OF_THE_VM>
```
Start the PowerShell prompt:

    pwsh

### Install the Az PowerShell Module

    Install-Module -Name Az -AllowClobber -Scope CurrentUser

Enter Y to continue installing from the PowerShell gallery. The installation process will take about three minutes.

### Connect the Azure Account and Create a VM
Connect to Azure:

    Connect-AzAccount

Copy the code provided in the terminal.

In the browser, navigate to https://microsoft.com/devicelogin.
Paste the code you copied.
Click Next.
Enter the Azure Portal credentials provided on the lab page.
Back in the terminal, enter the following to create a new Azure VM:

    New-AzVM `
    -ResourceGroupName '<RESOURCE_GROUP_NAME_PROVIDED_IN_LAB>' `
    -Name 'myvm1234' `
    -Location 'westus' `
    -VirtualNetworkName '<VIRTUAL_NETWORK_NAME_PROVIDED_IN_LAB>' `
    -SubnetName 'default' `
    -SecurityGroupName '<NSG_PROVIDED_WITH_LAB>' `
    -PublicIpAddressName 'myvm1234pubip' `
    -OpenPorts 80,3389


Hint: For the parameters above within <>, you can retrieve them by logging in to the Azure Portal and navigating to each resource via All resources or by searching.

Make up a username and password for the VM. It will take a few minutes to finish creating.

Note: The password must be between 12–72 characters long and contain three of the following requirements:

An uppercase character
A lowercase character
A numeric digit
A special character
In the Azure Portal, navigate to Virtual machines. We should see the one we just created listed.
