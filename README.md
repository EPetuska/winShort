# winShort
Shortcuts for Windows

# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands
# Use link above for official Microsoft Windows commands reference

# Help Commands
/? = used after a command to show information about the command\
help = used before a command to show information about the command but not as powerful as /?\

# Navigating Commands
cd = Change Directory\
cd.. = Moves you up one directory\
cd\ = Takes you to root of the volume you are working in\
md = Make Directory\
rd = Remove Directory\
dir = Directory command, used alone it displays the contents of the current directory\
tree = Shows all the directories and subdirectories from your current position\
copy = Copies one file from one location to another
    example: copy \documents\test.txt \desktop\projects\
        Now the original file test.txt is located in \documents\ and 
        a copy is in \desktop\projects\
xcopy = Command to copy large amounts of data from one location to another, can be used to copy entire directories\ 
robocopy = A directory replication tool. meant to copy directories that contain lots of data\
del = Delete a file\

# Partitioning and File System-based Commands
diskpart = Command line counterpart of the Windows' Disk Management program. Needs to run before any other diskpart\ actions can be used. Here you can create, delete, and extend volumes, assign drive letters, make a partition active.\ 
format =  Format hdd & ssd to the FAT, FAT32, or NTFS file systems\
defrag = Command line version of Disk Defragmenter, to analyze a drive type defrag -a\
convert = Command that enables you to convert a volume that was firnatted as FAT32 over to NTFS without losiing data\

# Repair
Chkdsk = checks a drive, fixes basic issues like lost files, and displays a status report, can alsos fix some errors on the drive by using the /F switch. /R switch locates bad sectors and recovers data\
SFC = System File Checker, Windows utility that checks protected system files. SFC /scannow scans all protected files immediately and repairs file. SFC /verifyonly scans the integrity of files but does not perform a repeir\

# Networking Commands
ipconfig = Displays current TCP/IP network configuration values, used to troubleshoot network connectivity\
ipconfig /all = Shows more information than ipconfig, including if DHCP is being used, DNS server address, & MAC address\
ipconfig /release = Release the current IP address from DHCP server\
ipconfig /renew = Request a new IP address from DHCP server\
ipconfig /flushdns = Erase the DNS cache\
ping = Tests whether another host is available over the network\
ping 127.0.0.1 or ping ::1 = Loopback address for IPv4 & IPv6 respectively, used to prove if the network adapter and TCP/IP have been installed properly\
ping -t = Pings the host intil the command is stopped\
ping -n = Pings a host a specific number of times, example ping -n 20 127.0.0.1\
ping -l = Pings the host but you can specify the number of bytes per packet to be sent\
ping -a = Resolves addresses to hostnames\
ping -4 = Forces the use of IPv4 and results in IPv4-based data\
ping -6 = Forces the use of IPv6 and reuslts in IPv6-based data\
arp = Address Resolution Protocol resolves between IP addresses and MAC addresses so that data communications can flow from the operating system to the physical network adapter.\
tracert = Trace Route, builds on ping in that it send packets to destinations beyond the local computer's network. It pings each router along the way between you and the final destination.\
netstat = Command that shows the network statistics for the local computer\
nbtstat = Displays network protocol statistics that use NetBIOS over TCP/IP connections\
nslookup = Queries DNS servers to discover DNS details, including the IP address of hosts\
net stop = Stop a service\
net start = Start a service\
net view = View which computers are currently available on the network\
net share = Command to share folders for other users to view\
net use = Command to view mapped network drive\

# Other Commands
tasklist = Shows all the processes running, similar to the Processes tab of the Task Manager\
taskkill = Used to shut processes down, need to find process ID \
dism = Deployment Image Servicing and management, used to scan and repair Windows operating system images or prepare and service Windows operating system images for deployment\
shutdown = Command to turn off the computer\
gpupdate = Updates group policy settings\
gpresult = Command displays the Resultant Set of Policy information for an ser and computer\
