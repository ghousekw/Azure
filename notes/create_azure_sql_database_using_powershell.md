# Creating Azure SQL Databases Using PowerShell
## Introduction

In this lab, we walk through using Azure PowerShell to create a SQL Database. This beginner-level hands-on lab covers several concepts, including the following.

- Creating variables to store key parameters.
- Identifying the proper cmdlets to create an Azure SQL Server and Azure SQL Database.
- Creating the Azure SQL Server and Database using the correct parameters.

This hands-on lab uses the Azure Cloud Shell, so there's no need to install any software. This way it's possible to follow along at work or home using the web browser.

## Connecting to the Lab:
- Log in to the Azure Portal using the credentials provided on the lab instructions page.
Create the Variables for the SQL Server and Database
Click the Cloud Shell icon (>_) at the top of the page.

- Click PowerShell.

- Click Show advanced settings.

- Use the combo box under Could Shell region to select West US.

- Under Storage account, click the radio button for Use existing.

- In the box under File share, enter "shell".

- Click Create storage.

## Identify the current resource group.

    get-azresourcegroup

Select the ResourceGroupName value and copy it to the clipboard.

Create a variable and set it to the value copied in the previous step.

    $resource = 'RESOURCE_GROUP_NAME'

Create a variable for the location.

    $location = 'westus'
Create a variable for the name of the SQL server.

    $name = 'sql01'

# Create the Azure SQL Server
Create the SQL Server.

    New-AzSqlServer `
    -ResourceGroupName $resource `
    -Location $location `
    -ServerName $name `
    -ServerVersion '12.0' `
    -SqlAdministratorCredentials (Get-Credential)

- Enter a user name of "azsqladmin" (without the quotes) when prompted.

- Provide a password when prompted.

If you receive an error that sql01 already exists, redefine $name as a unique name, and then rerun the first command in this task.

# Create the SQL Database
Create the database.

    New-AzSqlDatabase -ResourceGroupName $resource -ServerName $name -DatabaseName 'Database01'