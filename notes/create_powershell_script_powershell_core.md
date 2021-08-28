# Creating Your First PowerShell Script Using PowerShell Core

## Introduction

In this hands-on lab, you will create a PowerShell script that outputs process information to a CSV file. You will have to use the appropriate PowerShell commands to filter the processes that are consuming more than 2 MB of memory. Additionally, you will be required to output only the WorkingSet and ProcessName columns to the CSV file. Once you've created the CSV file, you can view the contents using the Get-Content cmdlet.

### Connect to the Linux VM and Create the File:
Open a terminal session and log in to the VM using the credentials provided:

    ssh cloud_user@<PUBLIC_IP>

Start a PowerShell session:

    pwsh

Create a file named processinfo.ps1:

    vim processinfo.ps1

>Hint: When copying and pasting code into Vim from the lab guide, first type :set paste to avoid adding unnecessary spaces and hashes.

### Create the PowerShell Script:
In the processinfo.ps1 file, enter:

    $ps = Get-Process

    $psinfo = $ps | Where-Object {$_.WorkingSet -gt 2mb} |
    Format-Table -Property WorkingSet, ProcessName

    $psinfo | out-file ./processinfo.csv
Save and quit by pressing Escape followed by :wq!.

### Run the Script and Verify the Contents:
Run the PowerShell script:

    ./processinfo.ps1

Make sure the file is there:

    dir

We should see it listed.

Open the file:

    Get-Content ./processinfo.csv