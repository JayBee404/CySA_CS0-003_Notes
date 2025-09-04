Spoofing attacks can be mitigated by configuring authentication for email server systems

Sender Policy Framework (SPF) - DNS record identifying hosts authorized to send mail for the domain with only one being allowed per domain
sample:
```
TXT @ v=spf1
mx include:_spf.google.com
include:email.freshdesk.com -all
```

DomainKeys Identified Mail (DKIM) - Provides a cryptographic authentication mechanism for mail utilizing a public key published as a DNS record

Domain-Based Message Authentication, Reporting, and Conformance (DMARC) - A framework for ensuring proper application of SPF and DKIM utilizing a policy published as a DNS record

DMARC can use either SPF or DKIM or both

Cousin Domain - A DNS domain that looks similar to another name when rendered by a Mail User Agent (MUA) similar method used in typosquatting attacks



