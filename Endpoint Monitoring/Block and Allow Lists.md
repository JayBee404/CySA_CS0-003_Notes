Blocklisting - The process of blocking known applications, services, traffic, and other transmissions to and from your systems
A security configuration where access is permitted unless the entity appears on a blocklist
Block lists are useful in incident response for their ability to block the source of malware

Cons of blocklisting:
1. Risk of false positives could block legitimate traffic
2. You don't know everything that should be blocked

Allowlisting - The process of allowing only known applications, services, traffic, and other transmissions to and from your systems
Allowlisting can be an effective fallback posture to use while conducting an incident response investigation

-- **Warning** -- 
Allow lists are incredibly restrictive and can prevent users and systems from transmitting data to new or changing recipients, so they need to be constantly fine-tunes to avoid interference with business operations
If you're using IP addresses on your allow list, this can also cause issues as many servers use multiple IP addresses and do load balancing

Use a block list method on a day-to-day basis

Application allowlisting can be useful to prevent unauthorized or malicious software from executing. Tends to be less dynamic than traffic, so maintaining the list requires less interaction

Execution Control - The process of determining what additional software may be installed on a client or server beyond its baseline. Can be configured as either a block or allow list

Software Restriction Policies (SRP) - Creates an allow list file for different system locations, where your executable and script files are allowed to be launched from
Another method for achieving this can be done by setting up rules configured with hash values of the programs

AppLocker - Used to improve the configuration options and defaults of the SRP

Windows Defender Application Control (WDAC) - Allows to create a code integrity policy, and this can be used on its own or in conjunction with AppLocker

Application control can also be achieved in Linux with the following:

Mandatory Access Control (MAC)

Linux Security Module (LSM)

SELinux and AppArmor are two well-known Linux security modules

Configuration Management - Allows for having a process in place of how we're going to update all of our block and allow lists for any of those changes
Large changes should be preceded by a risk assessment and business impact analysis 

