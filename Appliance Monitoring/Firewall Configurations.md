Screened Subnet - Physical or logical subnetwork that contains and exposes an organization's external-facing services to an untrusted network like the internet

ACLs are processed from top-to-bottom with the most specific rules at the top

Basic rules for configuring ACLs:
1. Block incoming requests from internal or private, loopback, and multicast IP ranges
2. Block incoming requests from protocols that should only be used locally (ICMP, DHCP, OSPF, SMB, etc.)
3. Configure IPv6 to either block all IPv6 traffic or allow it to only authorized hosts and ports

Drop Versus Reject - Deny rule can either drop a packet or explicitly reject it by sending a TCP RST or an ICMP port/protocol unreachable to the requester

Dropping traffic makes it harder for an adversary to identify port states accurately

Firewalking - Reconnaissance technique to enumerate firewall configuration and attempt to probe hosts behind it
Firewalking occurs when an attacker can find an open port on the firewall, then sends a packet with a TTL of one past the firewall to find its hosts. Blocking outgoing ICMP status messages can prevent firewalking.

Egress Filtering - Applies ACL rules to outgoing traffic to prevent malware from communicating with C2 servers

Best practices for configuring egress filters:
1. Only allow whitelisted application ports and destination addresses
2. Restrict DNS lookups to trusted and authorized DNS services
3. Block access to known bad IP address ranges
4. Block all Internet access form host subnets that don't use it (ICS/SCADA)

Black Hole - Means of mitigating DoS or intrusion attacks by silently dropping (discarding) traffic
Blackholing can be used to stop a DDoS attack at the routing layer by sending traffic to the null interface. Blackholing consumes less resources than an ACL but can cause collateral damage for legitimate users

Dark Nets - Unused physical network ports or unused IP address space within a local network often used by attackers
Redirect all dark nets to a black hole until they are needed for business operations

Sinkhole - DoS attack mitigation strategy that directs the traffic that is flooding a target IP address to a different network for analysis

Sinkholing is better than blackholing if you want to determine the cause of the DDoS attack

