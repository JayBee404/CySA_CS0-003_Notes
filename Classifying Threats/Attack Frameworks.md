Kill Chain - Describes the stages by which a threat actor progresses a network intrusion
1. Reconnaissance - The attacker determines what methods to use to complete the phases of the attack.
2. Weaponization - The attacker couples payload code to enable access with exploit code, which will then use a vulnerability to execute on the target system.
3. Delivery - The attacker identifies a vector to transmit the weaponized code to the target environment.
4. Exploitation - The weaponized code is executed on the target system.
5. Installation - Enables the weaponized code to run a remote access tool and achieve persistence on the target system.
6. Command & Control - The weaponized code establishes an outbound channel to a remote server that can then be used to control the remote access tool and possibly download additional tools to progress the attack.
7. Actions on Objectives - The attacker typically uses the access he has achieved to covertly collect information from the target systems and transfer it to a remote system (data exfiltration) or achieve other goals and motives.

MITRE ATT&CK Framework - A knowledge base that lists and explains specific adversary TTPs.

The pre-ATT&CK tactics matrix aligns with the reconnaissance and weaponization phases of the Kill Chain.

Diamond Model of Intrusion Analysis - A framework for analyzing cybersecurity incidents and intrusions by exploring the relationships between four core features: adversary, capability, infrastructure, and victim.