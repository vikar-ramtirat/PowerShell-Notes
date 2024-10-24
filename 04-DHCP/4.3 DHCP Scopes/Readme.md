# DHCP Scopes

Create a Scope

    Add-DhcpServerv4Scope -Name 'Azure Studio' -StartRange 10.1.230.100 -EndRange 10.1.230.150 -SubnetMask 255.255.255.0
    Add -ComputerName <Name> to point to the DHCP server if commands are being executed remotely

Delete a scope

    Remove-DhcpServerv4Scope -ScopeId 10.1.230.0

Configuring scope options

    Set-DhcpServerv4OptionValue -ScopeId 10.1.230.0 -DnsServer 10.1.230.11 -DnsDomain LearnAzureStepByStep.com -Router 10.1.230.1

More examples available on - https://learn.microsoft.com/en-us/powershell/module/dhcpserver/set-dhcpserverv4optionvalue?view=windowsserver2022-ps

Enable/disable scope

    Set-DhcpServerv4Scope -ScopeId 10.1.230.0 -State <Active/Inactive>

