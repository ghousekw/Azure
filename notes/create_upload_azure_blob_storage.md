# Create Azure Blob Storage and Upload a Blob
## Introduction
- In this lab, we walk through setting up Azure Blob Storage in Azure. This beginner level hands-on lab covers several concepts: Azure storage accounts, Azure containers, and Azure blobs.

## Solution
- Log in to the Azure portal using the credentials provided on the lab instructions page.

## Create a Storage Account
1. In the main menu search bar, type and select storage accounts.
1. Click + Create.
1. Set the following values:
    - Resource group: Existing resource group
    - Storage account name: unique name (Use Azure Resource Naming Conventions)
    - Region: (US) East US 2
    - Performance: Standard
    - Redundancy: locally-redundant storage (LRS)
1. Click Next: Advanced > Next: Networking > Next: Data protection.
1. Scroll down to Tracking and click Enable soft delete for blobs.
1. Click Next: Tags > Next: Review + create >
1. Once validation passes, click Create.

**Note**: Deployment may take several minutes.

## Create a Blob Container
1. Once deployed, click *Go to resource.
1. On the left menu under Data storage, click Containers.
1. Click + Container.
1. In Name, enter "images" and click Create.

## Upload a Blob
1. Select the images container.
1. Click Upload.
1. Click the folder icon and select the file to upload from your local filesystem.
1. Click Open.
1. Click Upload.

**Note**: If the blob doesn't immediately appear, click Refresh.

6. Click the newly uploaded blob to open it.
1. In the Overview tab next to URL, click the copy icon and paste the blob URL in the address bar of a new browser tab.

- An error message should display indicating that the blob data is private.