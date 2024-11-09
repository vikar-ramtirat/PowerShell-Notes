# Performing Bulk Operations


   Bulk Operations for setting Department

    Get-ADUser -Filter {-not(department -like "*")} | Set-ADUser -department "IT"

   Bulk Operations for disabling accounts not logged in for 90 days

    $logonDate = (get-date).addDays(-90)
    Get-ADUser -Filter{lastLogon -le $logonDate} | Disable-Account