# Creating Azure Virtual Machines Using PowerShell

## Introduction

In this lab, we walk through using Azure PowerShell to create a virtual machine. This beginner-level hands-on lab covers several concepts, including the following.

    * Creating an Azure virtual machine with PowerShell.
    * Obtaining the public IP address of the virtual machine.
    * Logging into the virtual machine via remote desktop.

This hands-on lab uses the Azure Cloud Shell, so there's no need to install any software. This way it's possible to follow along at work or home using the web browser.
Connecting to the Lab

    Log in to the Azure Portal using the credentials provided on the lab instructions page.

## Create a Virtual Machine

1. Click the Cloud Shell icon (>_) at the top of the page.

2. Click PowerShell.

3. Click Show advanced settings.

4. Use the combo box under Could Shell region to select West US.

5. Under Storage account, click the radio button for Use existing.

6. In the box under File share, enter "shell".

7. Click Create storage.

Get the name of the resource group.

    Get-AzResourceGroup

Copy the value for the ResourceGroupName parameter to the clipboard.

Create the new virtual machine with the following parameters. For RESOURCE_GROUP_NAME, paste in the name copied in the previous step.

    new-azvm -ResourceGroupName 'RESOURCE_GROUP_NAME' `
    -Name 'TestVM' `
    -VirtualNetworkName 'MyVNet' `
    -SubnetName 'MySubnet' `
    -SecurityGroupName 'MySecurityGroup' `
    -PublicIpAddressName 'myPubIP' `
    -OpenPorts 80, 3389

Provide a username of "azureuser" when prompted and provide a password.

Obtain the Public IP Address

Get the public IP address.

    Get-AzPublicIpAddress