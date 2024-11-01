# Creating Child Domain

    Installing Active Directory Domain Services

        Install the AD-DS role
        Install-windowsfeature -name AD-Domain-Services –IncludeManagementTools


    List available commands

       Get-command –module ADDSDeployment

    Promoting a DC
     Create a child domain

        Install-ADDSDomain -NewDomainName lab -ParentDomainName LearnAzureinSteps.com -Credential (Get-Credential)
        Install-ADDSDomain -NewDomainName lab -ParentDomainName LearnAzureinSteps.com -InstallDNS -CreateDNSDelegation -DomainMode Win2012R2 -ReplicationSourceDC DC1.LearnAzureinSteps.com -SiteName London -DatabasePath "D:\NTDS" -SYSVOLPath "D:\SYSVOL" -LogPath "E:\Logs" -SkipPreChecks -NoGlobalCatalog -Credential (Get-Credential)

    https://learn.microsoft.com/en-us/powershell/module/addsdeployment/install-addsdomain?view=winserver2012r2-ps&redirectedfrom=MSDN