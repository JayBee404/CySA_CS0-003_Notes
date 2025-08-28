Known-bad IP Address - IP address or range of addresses that appears on one or more block lists.

Domain Generation Algorithm (DGA) - Method used by malware to evade block lists by dynamically generating domain names for C2 networks.
1. Attacker sets up one or more Dynamic DNS (DDNS) services
2. Malware code implements a DGA to create a list of new domain names
3. A parallel DGA is used to create name records on the DDNS service
4. The malware tries a selection of the domains it has created to connect to C2
5. C2 server communicates with a new seed for the DGA to prevent being blocked

Fast Flux Network - Method used by malware to hide the presence of C2 networks by continually changing the host IP addresses in domain records using domain generation algorithms.

Easy detections for DGA/FFN:
1. High number of random-string domains (124nifs78.net, etc.)
2. High rate of NXDOMAIN errors when resolving the DNS, could be an indicator of DGA

Secure Recursive DNS Resolver - Allows one trusted DNS server to communicate with other trusted DNS servers to search for an IP address and return it to the client.

