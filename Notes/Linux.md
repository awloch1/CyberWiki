### Commands:
`touch` -  create file
`mkdir` - create directory
`pwd` - print working directory
`ls` - listing
`cat` - read file
`wc` - count lines
`kill <PID>` - ends proces with defined PID
`systemctl [option] [service]` - this command allows us to interact with the **systemd** process/daemon
`Ctrl + Z` - stop the current process and send it to the background
`fg` - resume execution in the foreground
`bg` - resume execution in the background
`crontab -e` - allows to add/edit crontab with format `min hour day month weekday command`
`ifconfig` - shows ip configurations
##### Viewing Processes
`ps` - shows list of the running processes 
**options:**
- **a** - Show processes for all users with a terminal.
- **u** - Display detailed user-oriented information (user, CPU, memory, etc.).
- **x** - Include processes without a controlling terminal (background services/daemons).
##### Find: 
`find -name <name>` - find by filename
##### Grep:
search in file content
`grep "example" test.log` - shows entry with word "example"  in the file test.log

options:
`-R` - search for a variable across **all files** in the current directory and its subfolders

##### Downloading files
`wget <address of the resource>`

##### Transferring files using SSH
 `scp <source file> <username@ip:/<destination file>`

### Operators
`&` - run commands in the background
`&&`- multiple commands
`>` - replace output
`>>` - append output


### Common Directories
**/etc**
- Stores system configuration files
- Example files
	- `passwd`->  User accounts
	- `shadow` -> encrypted passwords
	- `sudoers` -> sudo permissions

**/var**
- Stores variable data 
- Used for logs and service data
- Example:
	- `/var/log` -> system logs
	- `/var/backups` -> backups

**/root**
- Home directory of the root user
- Only accessible by root

**/tmp**
- temporary files directory
- Cleared after reboot
- **Writable by all users**

### Shell
**To switch between these shells, you can type the shell name that is present on your OS**
**Use `./` before the script name to execute it.**

`echo $SHELL` - prints which shell you are using
`/etc/shells` - contains all the installed shells
`chsh -s /usr/bin/zsh` - permanently change your default shell

**BASH**
`history`- display all your previous commands.
`#!/<shell path>` - Every script should start by defining interpreter
`read <name>` - take input from the user
`#` - comment

Loop:
```shell
for i in {1..10};
do
echo $i
done
```

If conditions:
```shell
if [ "$name" = "Stewart" ]; then
        echo "Welcome Stewart! Here is the secret: THM_Script"
else
        echo "Sorry! You are not authorized to access the secret."
fi
```