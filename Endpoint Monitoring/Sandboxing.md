Sandboxing - A computing environment isolated from a host system to guarantee that the environment runs in a controlled, secure fashion and that communication links between the sandbox and the host are usually completely prohibited

- Determine if the file is malicious
- Determine effects on the system
- Identify dependencies

Sandboxing allows you to quickly test malware in multiple environments

- Monitor system changes
- Execute known malware
- Identify process changes
- Monitor network activity
- Monitor system calls
- Create snapshots
- Record file creation/deletion
- Dump virtual machine's memory

FlareVM - Allows you to run a Windows binary on the system and see what the status is and all the different changes the malware is doing

Cuckoo - Allows you to automatically run different malware samples and see what they do inside of a Linux, Windows, or a Mac environment

Joe Sandbox - Allows a security research or cybersecurity analysts to analyze and understand the behavior of malware samples in a safe and controlled environment. Emulates the environment of a real computer and allows malware samples to be run and analyzed in a safe and isolated environment. One of the key features of Joe Sandbox is its ability to detect and analyze malware across multiple platforms, including Windows, Mac OS, Linux, and Android

For complex analysis, you may need to create a honeypot lab with multiple sandboxed machines and Internet access to study malware and its C2