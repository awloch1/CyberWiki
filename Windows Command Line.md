`ver` - prints OS version
`systeminfo` - list informations about OS
`cls` - clear screen
`ipconfig /all` - shows information about network configuration
`tracert <target name>`- traces the network route
`netstat` - displays current network connections and listening ports
	`-a` displays all established connections and listening ports
	`-b` shows the program associated with each listening port and established connection
	`-o` reveals the process ID (PID) associated with the connection
	`-n` uses a numerical form for addresses and port numbers
`nslookup` - finds the IP address of a domain name.
`dir` - shows the child directories
	`/a` - Displays hidden and system files as well.
	`/s `- Displays files in the current directory and all subdirectories.
`tasklist` - lists running processes
`tasklist /FI "imagename eq test.exe"` - filters for processes with test.exe name
`taskkill /PID target_pid` - kills process with target PID

**directories**
`mkdir` - create directory
`rmdir` - remove directory

**files**
`type` - view text file
`copy <source file> <new file>` - copy file
`move <file name> <destination>` - move file
`del/erase` - delete file

**pipes**
`| more` - will display a single page and wait for you to press Spacebar