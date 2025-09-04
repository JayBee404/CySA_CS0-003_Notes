Sysinternals - A suite of tools designed to assist with troubleshooting issues with Windows, and many of the tools are suited to investigating security issues

You must first understand what legitimate processes are used by a system to identify suspicious ones

System Idle (PID 0) and System (PID 4) - Kernel-level processes and binaries that are used as the parent of the first user-mode process (smss.exe (Session Manager SubSystem))

Client Server Runtime SubSystem (csrss.exe) - Manages low-level Windows functions and it is normal to see several of these running (as long as they are launched from %SystemRoot%\System32 and have no parent)

WinInit (wininit.exe) - Manages drivers and services and should only have a single instance running as a process

Services.exe - Hosts nonboot drivers and background services and should only have one instance running as a child of wininit.exe (other service processes can also be a child of services.exe or svchost.exe)

Anytime you look at services, they should be started by NT AUTHORITY/SYSTEM, LOCAL SERVICE, or NETWORK SERVICE accounts and not user/admin accounts

Local Security Authority SubSystem (lsass.exe) - Handles authentication and authorization services for the system, and should have only a single instance running as a child of wininit.exe

WINLOGON (winlogon.exe) - Manages access to the user desktop and should have only one instance for each user session with the Desktop Window Manager (dwm.exe) as a child process in modern versions of Windows

USERINIT (userinit.exe) - Sets up the shell (typically explorer.exe) and then quits, so you should only see this process briefly after logon

Explorer (explorer.exe) - The typical user shell launched with the user's account privileges rather than SYSTEM's which is likely to be the parent for all processes started by the logged-on user

What might make a process look suspicious?
1. Any process name that you do not recognize/cannot find information on easily
2. Any process name that is similar to a legitimate system process (scvhost instead of svchost)
3. Processes that appear without an icon, version information, description, or company name
4. Processes that are running unsigned binaries, especially if from a well-known company like Microsoft
5. Any process whose digital signature doesn't match the identified publisher
6. Any process that does not have a parent/child relationship with a principal Windows process
7. Any process hosted by Windows utilities like Explorer, Notepad, Task Manager, etc.
8. Any process that is packed (compressed), highlighted purple in Process Explorer

What do you do when you find a suspicious process?
1. Identify how the process interacts with the Registry and file system
2. How is the process launched?
3. Is the image file/binary located in the system folder or a temp folder?
4. What files are being manipulated by the process?
5. Does this process restore itself upon reboot after deletion?
6. Does a system privilege or service get blocked if you delete the process?
7. Is the process interacting with the network?
8. 