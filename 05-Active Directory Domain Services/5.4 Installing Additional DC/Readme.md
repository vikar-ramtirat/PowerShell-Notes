# Installing Additional DC

 Installing Active Directory Domain Services
    
    Install the AD-DS role

        Install-windowsfeature -name AD-Domain-Services –IncludeManagementTools

    List available commands
        Get-command –module ADDSDeployment

    Promoting a DC

     Add an additional domain controller

        Install-ADDSDomainController -InstallDns -DomainName LearnAzureStepbyStep.com


    Add a Read-only domain controller

       Install-ADDSDomainController -InstallDns -DomainName LearnAzureStepbyStep.com -ReadOnlyReplica -DelegatedAdministratorAccountName "lab\Vikar" -AllowPasswordReplicationAccountName "" -UseExistingAccount     


  https://learn.microsoft.com/en-us/powershell/module/addsdeployment/install-addsdomaincontroller?view=winserver2012r2-ps&redirectedfrom=MSDN

