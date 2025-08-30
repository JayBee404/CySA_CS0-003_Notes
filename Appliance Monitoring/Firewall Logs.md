Access Control List - List of permitted and denied network connections based on IP addresses, ports, or applications in use.

Firewall logs can provide 4 main points of useful data:
1. Connections that are permitted or denied
2. Port and protocol usage on the network
3. Bandwidth utilization with the duration and volume of usage
4. An audit log of the network or port address translations (NAT/PAT) that occurred

iptables - Linux-based firewall that uses the syslog file format for its logs

Code | Severity | Description
0 | Emergency | System is unusable
1 | Alert | Action must be taken immediately
2 | Critical | Critical conditions
3 | Error | Error conditions
4 | Warning | Warning conditions
5 | Notice | Normal but significant condition
6 | Informational | Informational messages
7 | Debug | Debug-level messages

Windows Firewall - Windows-based firewall that uses the W3C Extended Log File Format

Employ a log collection tool to gather the large volume of firewall logs for later analysis

Blinding Attack - condition that occurs when a firewall is under-resourced and cannot log data fast enough, therefore some data is missed

Log retention is determined by the number of events generated and available storage capacity

