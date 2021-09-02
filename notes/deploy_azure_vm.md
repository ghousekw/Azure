# Creating Your First Azure Virtual Machine
## Introduction

In this hands-on lab, we will use the Azure Portal to create and use a virtual machine.

We will log in to the Azure Portal and create a virtual machine, a virtual network, and a network interface card for the virtual machine. Then, we will connect to the virtual machine via RDP. Finally, we will use the Azure Portal to turn the virtual machine off.

After completing this lab, you will have gained the experience required to create and use your first virtual machine using the Azure Portal.

To connect to a Windows VM from a Mac, you will need an RDP client for Mac such as Microsoft Remote Desktop (https://aka.ms/rdmac). For more information on how to connect, see: https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-mac.

Linux users can optionally use a program like Remmina: You can find it at: https://remmina.org/

# Log In to the Azure Portal
- On the lab instructions page, click Open Azure Portal.
- On the Azure Portal sign-in page, enter the username you were provided on the lab instructions page.
- Click Next.
- Enter the password you were provided on the lab instructions page.
- Click Sign in.
- In the Welcome to Microsoft Azure message box, click Maybe later.
# Create a Virtual Machine
- On the Azure Portal home page, click Create a Resource.
- Select Windows Server Datacenter 2016
- In the Basics tab, configure the following settings:
    - Resource group: (Select the pre-provisioned group from the dropdown.)
    - Location: Leave the region the same as your Resource Group's region.
    - Virtual machine name: (Give the virtual machine a unique name.)
    - Image: Windows Server 2016 Datacenter Gen1
    - Size: Standard DS1_v2
    - Username: acg-admin
    - Password: Admin123456!
    - Confirm password: Admin123456!
- Click Next : Disks >.
    - In the Disks tab, configure the following settings:

    - OS disk type: Premium SSD
- Click Next : Networking >.

    - If for some reason port 3389 is not automatically filled in, for "Public Inbound Ports" select "Allow selected ports" and then for "Selected Inbound Ports" use the drop to choose "RDP 3389"
- Click Next : Management >.
- Click Next : Advanced >.
- Click Next : Tags >.
- Click Next : Review + create >.
- Click Create.
- Click the notifications icon at the top of the screen to monitor the deployment.
    - Wait a few minutes for the status to change to Your deployment is complete.

# Connect to the Virtual Machine
- Click All resources in the left sidebar.
- Click the name of our virtual machine to open it.
- Click Connect at the top of the page.
- Click Download RDP File. 
>Note: You have to wait a few minutes before you will be able to connect even if the VM shows as ready.

- Execute the RDP file either from the folder is was downloaded to, or your browser if it allows it 
>Quick Note: If you are on a Mac, make sure you are using the latest remote desktop tool which can be found at this URL. https://apps.apple.com/app/microsoft-remote-desktop/id1295203466?mt=12

- In the Enter your credentials menu, enter the following:
    - User name: acg-admin
    - Password: Admin123456!
- Click OK.
- Click Yes.

- Wait a few minutes for the virtual machine connection to be established.
# Turn Off the Virtual Machine
- Go back to the Azure Portal in your browser.
- In the virtual machine menu, click Stop.
- Click OK.
    - Wait a few moments, and refresh the menu until the status changes to Stopped (deallocated).

