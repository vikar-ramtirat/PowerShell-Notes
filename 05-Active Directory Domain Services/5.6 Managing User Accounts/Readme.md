# Managing User Accounts

 Create/Modify/Delete User Accounts

  Create
  
    New-ADUser Vikar Ramtirat

    New-ADUser –Name “Vikar Ramtirar” –GivenName Vikar –Surname Ramtirat –UserPrincipalName vikar.ramtirat@learnazureinSteps.com –SamAccountName VikarRamtirat –Enabled 1 –AccountPassword (Read-Host –AsSecureString “Password”)

  Modify

    Set-ADUser -Identity "VikarRamtirat" -Manager "VikarRamtirat"
    Get-ADUser -Identity "VikarRamtirat" | Set-ADUser -Manager "VikarRamtirat"

  Delete
    Remove-ADUser -Identity VikarRamtirat
