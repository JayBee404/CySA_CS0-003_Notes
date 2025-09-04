Syslog - A protocol for enabling different appliances and software applications to transmit logs or event records to a central server

Syslog follows a client-server model and is the de facto standard for logging of events from distributed systems

Syslog runs on most operating systems and network equipment using port 514 (UDP) over TCP/IP

A syslog message contains a PRI code, header, and message portion
 - A PRI code is calculated from the facility and severity level of the data
 - A header contains the timestamp of the event and the hostname
 - The message portion contains the source process of the event and related content

Since syslog relied on UDP, there can be delivery issues within congested networks

Basic security controls like encryption and authentication are not included by default within syslog

Due to these security issues, newer syslog implementations added new features and capabilities
1. Newer implementations can use port 1468 (TCP) for consistent delivery
2. Newer implementations can use TLS to encrypt messages sent to servers
3. Newer implementations can use MD5 or SHA-1 for authentication and integrity
4. Newer implementations can use message filtering, automated log analysis, event response scripting, and alternate message formats

The newer version of the server is called syslog-ng or rsyslog

Syslog can refer to the protocol, server, or the log entries themselves