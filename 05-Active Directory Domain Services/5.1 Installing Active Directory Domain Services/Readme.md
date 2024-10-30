# Installing Active Directory Domain Services

  Install the AD-DS role

   Install-windowsfeature -name AD-Domain-Services –IncludeManagementTools

  List available commands

   Get-command –module ADDSDeployment

  Promoting a DC
   Create a new forest
 
    Install-ADDSForest -DomainName LearnAzureinSteps.com -InstallDNS
    Install-ADDSForest -DomainName LearnAzureinSteps.com -CreateDNSDelegation -DomainMode Win20012R2 -ForestMode Win2012R2 -DatabasePath "d:\NTDS" -SysvolPath "d:\SYSVOL" -LogPath "e:\Logs"
    https://learn.microsoft.com/en-us/powershell/module/addsdeployment/install-addsforest?view=winserver2012r2-ps&redirectedfrom=MSDN