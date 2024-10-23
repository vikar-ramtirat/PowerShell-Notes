# 2.8 File Operations

Command output to a file
    get-process | out-file -filepath F:\Scripts\process.txt
    get-process | out-file F:\Scripts\process.txt -noclobber
    get-process | out-file F:\Scripts\process.txt -noclobber -append

Output file to screen
    get-content f:\scripts\computers.txt | out-string


#Installing IIS on a few servers mini Script

#1.Set Variable with path to file with server name
$hosts = Get-Content -Path C:\Scripts\hosts.txt

#2.Run command with script block to install IIS
Invoke-Command -ComputerName $host -ScriptBlock (Install-WindowsFeature Web-Server -IncludeManagementTools)

Extra Help
https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/out-file?view=powershell-7.4
