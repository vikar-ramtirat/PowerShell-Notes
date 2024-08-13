# 1.3 Aliases

#Alternate name for a cmdlet

#Easier to use

#Backwards compatibility

#Example

dir alias of Get-ChildItem

cd alias of Set-Location

#List aliases

Get-Alias

Set-Alias <alias> <command>

Set-Alias edit C:\Windows\System32\Notepad.exe

edit filename.txt

Remove-Item alias:edit

#Aliases don't support command line modifiers

#Use a function instead

#Save aliases to your profile