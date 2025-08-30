Most IDS/IPS systems will output logs in one or several of the following:
1. Unified output (machine readable)
2. Syslog
3. CSV
4. Tcpdump (pcap)
5. Input into a SIEM

**Snort Rule Format**:
Action Protocol SourceIP SourcePort Direction DestinationIP DestinationPort (RuleOption; RuleOption; ...)

- Action - alert, log, pass, drop, reject
- Direction - can be unidirectional (->) or bidirectional (<>)
- RuleOption - msg, flow, flags, track, reference, classtype, sid, rev

Sample snort rule for brute force attempts against IMAP mailbox accounts:
`alert tcp $EXTERNAL_NET any -> $HOME_NET 143 (msg:"PROTOCOL-IMAP logon brute force attempt"; flow:to_server,established,no_stream; content:"LOGON"; fast_pattern:only; detection_filter:track by_dst, count 30, seconds 30; metadata:ruleset community, service imap; reference:url,attack.mitre.org/techniques/T1110;classtype:suspicious-logon; sid:2273; rev:12;)`

