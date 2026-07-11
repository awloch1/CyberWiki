`Win + R`  - run dialog command
`Ctrl + Shift + Esc` - open task manager
### Windows Directory
command: `Win + R -> %windir%`

Stores important Windows system files and configuration.
**Important contents:**
- `System32` → core system files, DLLs, executables
- `SysWOW64` → 32-bit files on 64-bit Windows
- `Temp` → temporary system files
- `Fonts` → installed fonts
- `Logs` → system logs
- `WinSxS` → Windows component store and updates
### System Configuration
**Command:** `Win + R -> MSconfig`

Purpose: 
- Diagnose startup issue 
- Configure boot options
- manage system services

Key tabs:
- **general** - startup mode
- **Boot** - boot configuration
- **Services** - enable/disable services
- **Tools** - quick access to admin tools

`Win + R -> shell:startup` - open startup folder

Most startup options are now in Task Manager since Win10

### Advanced system settings

Purpose:
- control the performance behavior and system recovery

Key tabs:
 - Advanced -> Performance(settings) - view or modify [[#^pagefile|Page file]]
 - Advanced -> Startup and Recovery(settings) - view or modify the crash dump settings

### Computer Management
command: `Win + R  -> compmgmt.msc`

**System Tools**
- Task Scheduler - create and manage common tasks at the times we specify.
- Event viewer - allows us to view events that have occurred on the computer.
- Shared Folders- complete list of shares and folders shared that others can connect to.
- Local Users and Groups - same as.`lusrmgr.msc`
- Performance(`perfmon.mcs`) - view performance data either in real-time or from a log file
- Device Manager - view and configure the hardware, such as disabling any hardware attached to the computer.
- Storage:
	- Disk Management - enables you to perform advanced storage tasks like **- Set up a new drive**, **Extend/Shrink a partition**,**Assign or change a drive letter**

### System Information
Command `Win + R  -> Msinfo32.exe`
- Hardware Resources
- Components - specific information about the hardware devices installed on the computer
- Software Enviroments - shows information about installed software, [[#^environmentVariables|environment variables]] , and network connections.

### System Information
Command `Win + R -> resmon`
displays real-time information about CPU, memory, disk, and network usage.

### Windows Registry
Command `Win + R -> regedit`
- Central database that stores Windows settings and configuration
- Contains information about users, software, hardware, and system settings


### Definitions

**Page file** - file with extra virtual memory space when the physical RAM becomes full. ^pagefile

**service** - special type of application that runs in the background ^service

**environment variables** - stores data that is used by the operating system and other programs ^environmentVariables
