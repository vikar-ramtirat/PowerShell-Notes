# Import Export VMs

 Importing / Exporting VMs

    Export-VM –Name Azurevm-DC2 –Path C:\Exported
    Import-VM -Path C:\Exported\Azurevm-DC2\Virtual Machine\2F87C74EF5C6-4463BE35-7B6464D9E525.XML -Copy

 If there are errors during import

    $Report = Compare-VM -Path C:\Exported\Azurevm-DC2\Virtual Machine\2F87C74EF5C6-4463BE35-7B6464D9E525.XML -copy
    $report.Incompatibilities | Format-Table -AutoSize