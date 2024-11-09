# Import Export Data

Import examples

https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/import-csv?view=powershell-7.4


NewUser.ps1 Script using Import

$csvfile = "c:\Scripts\newUsers.csv"
$OU = "ou=UserAccounts,dc=learnazureinsteps,dc=net"

$users = Import-csv $csvfile

Foreach ($i in $users) {
    $DisplayName = $i.FirstName + " " + $i.LastName
    $SecurePass = ConvertTo-SecureString $i.DefaultPassword -AsPlainText -Force
    New -AdUser -Name $i.FirstName -Given $i.FirstName -Surname $i.LastName -DisplayName $DisplayName -Displayname -Department $i.Department -Path $OU -Account Password $SecurePass -Enabled $true
}


Export Examples

https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/export-csv?view=powershell-7.4