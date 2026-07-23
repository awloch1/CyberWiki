PowerShell is a powerful tool from Microsoft designed for task automation and configuration management. 

`Get-command` - lists all available [[#^cmdlets|cmdlets]], functions, aliases and scripts that can be executed in the current PowerShell session.
`-CommandType "Function"` - display only the available commands of type “function”
`Get-Help <command>` - shows detailed information about cmdlets
`Get-Alias` -  lists all aliases available
`Find-Module -Name "PowerShell*"` - allows you to search for modules (collections of cmdlets) in online repositories
`Install-Module -Name "PowerShellGet"` - command that allows you download and install from repository
`New-Item -Path "<path>" -ItemType "<type>"` - create item
`Remove-Item -Path "<path>"` -remove item
`Get-Content` - display the contents of file
`Select-String -Path ".\captain-hat.txt" -Pattern "hat"` - searches for text patterns within files

**System and Network Information Commands:**
`Get-ComputerInfo` - retrieves comprehensive system information
`Get-LocalUser` - lists all the local user accounts on the system
`Get-NetIPConfiguration` - provides detailed information about the network interfaces on the system, including IP addresses, DNS servers, and gateway configurations.
`Get-NetIPAddress` - show details for all IP addresses configured on the system, including those that are not currently active.
`Get-Process` - provides a detailed view of all currently running processes
`Get-Service` - provides a detailed view of all currently running services
`Get-NetTCPConnection` -  displays current TCP connections
`Get-FileHash` - calculates the hash value of a file to verify its integrity or detect changes.


`Get-Item -Path "C:\House\house_log.txt" -Stream *` - allows you to  view the Alternate Data Streams (ADS) attached to a file
### Pipes
`| Where-Object -Property "<Property Name>"` - pipe that filters objects based on specified conditions
	Example Properties:
		- `"Name" -like "ship"`
		- `"Extension" -eq ".txt"`

`| Select-Object Name,Length` -  is used to select specific properties from objects or limit the number of objects returned

`| Sort-Object Length` -  sorts objects by their **Length**

**comparison operators:**
- -ne -> not equal
- -gt -> greater than
- -ge -> greater than or equal to
- -lt -> less than
- -le -> less than or equal to

### Definitions

**cmdlets** - `command-lets` are lightweight PowerShell commands that perform a specific task, usually written in a **Verb-Noun** format, such as `Get-Process`^cmdlets