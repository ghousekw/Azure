# Working with Variables and Pipelines in Azure PowerShell

## Introduction

In this lab, we walk through using Azure PowerShell to work with variables and pipelines. This beginner-level hands-on lab covers several concepts, including:

- Azure PowerShell syntax.
- Azure PowerShelI help.
- Azure PowerShell default and assumed parameters.

### Connecting to the Lab
- Log in to the Azure Portal using the credentials provided on the lab instructions page.

Create a Variable to List the Azure resources

- Click the Cloud Shell icon (>_) at the top of the page.
- Click PowerShell.
- Click Show advanced settings.
- Use the combo box under Could Shell region to select West US.
- Under Storage account, click the radio button for Use existing.
- In the box under File share, enter "shell".
- Click Create storage.

Set the $Resources variable.

    $Resources=Get-AzResource

Create a Variable to Show the Date
Create and set the $Today variable.

    $Today=(Get-Date).DateTime

Verify the $Today variable.
    
    $today

Display the Azure Resources List and Filter the List Based on Kind and Location Display the entire list of resources.

$Resources Format the list of resources into a list.

    $Resources | Format-List

Display just the name of the resources.

    $Resources | Format-Wide

Filter the resources to only show resources with a Kind of Storage.

    $Resources | Where-Object {$_.Kind -eq 'Storage'}

Filter the resources to only show resources with a Kind not equal to Storage.

    $Resources | Where-Object {$_.Kind -notlike 'Storage'}

Filter the resources to only show resources with a Location of westus.

    $Resources | Where-Object {$_.Location -eq 'westus'}