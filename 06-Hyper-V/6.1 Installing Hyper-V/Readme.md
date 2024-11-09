# Installing Hyper-V

    Installing Hyper-V

        Install-WindowsFeature -Name Hyper-V -IncludeManagementTools -Restart

    Verify Install

        Get-Service vmms
        Get-VMHost
        Get-VM