Diamond Model of Intrusion Analysis


Diamond Model Vertices With Supporting Evidence

| Diamond Vertex   | Description | Supporting Evidence (from typical reports: Mandiant, CISA, APTNotes) |
|------------------|-------------|------------------------------------------------------------------------|
| **Adversary**    | The threat actor performing the intrusion. | • TTPs consistent with known groups (e.g., APT29, FIN7)  
|                  |             | • Malware development style / unique coding patterns  
|                  |             | • Infrastructure reuse patterns  
|                  |             | • Operational tempo, targeting profile  
|                  |             | • Intelligence reports linking activity to a known adversary |
| **Capability**   | Tools, malware, exploits, scripts, techniques used. | • Malware samples (hashes, YARA signatures)  
|                  |             | • Exploit chain (CVE evidence, exploit logs)  
|                  |             | • Command sequences (PowerShell, Bash scripts)  
|                  |             | • Dropper, loader, C2 protocol details  
|                  |             | • MITRE ATT&CK technique mappings |
| **Infrastructure** | Systems the adversary uses to deliver capabilities or interact with victims. | • C2 domain names and IPs  
|                  |             | • Hosting provider records  
|                  |             | • Beaconing traffic logs  
|                  |             | • DNS records, passive DNS, WHOIS  
|                  |             | • VPN / proxy usage patterns  
|                  |             | • Email infrastructure used for phishing |
| **Victim**       | Target of the adversary. | • Affected organizations or individuals  
|                  |             | • Sector (e.g., healthcare, government, finance)  
|                  |             | • Geography of targeted entities  
|                  |             | • Compromised assets (servers, endpoints, cloud accounts)  
|                  |             | • Vulnerabilities exploited on victim environment |


Summary of The Threat Actor’s Profile

This report describes a cyber attack carried out by a hacking group known as APT29. This group is very advanced and is believed to be supported by a national government. Their main goal is cyber espionage, which means stealing secret information.
They typically target organizations like:
• Government agencies
• Embassies and diplomatic groups
• Companies that work with the defense sector
• Think tanks and policy organizations

They focus most of their efforts on government sectors in the United States and Europe.
How the Attack Started
The hackers got into the network by sending targeted phishing emails. These emails contained a link. When clicked, the link took the victim to a hacked website that installed 
malicious software called "EnvyScout." This method is a common way that APT29 operates.

Analyzing the Attack
Using a security model, we can break down the attack:
• The Hacker: APT29
• Their Tools: They used the EnvyScout malware to get in, and then other programs to maintain control.
• Their Infrastructure: They used compromised websites and special domains to hide their location and make it hard to track them.
• The Victim: U.S. federal agency staff, which fits the group's usual targets.

How to Protect Against Such Attacks
Security agencies recommend these steps to defend against groups like APT29:
• Use multi-factor authentication (MFA) for all accounts.
• Improve email security to better detect and block malicious messages.
• Monitor computer networks for signs of the known malicious websites, links, and software used in this attack.
• Segment networks so if hackers get in, they can't easily move everywhere.
• Control what kind of traffic can leave the network to block communication with the hackers.
• Actively search for suspicious activity, like unusual logins or system commands.

Using these security measures together can greatly reduce the risk of a successful attack by this hacking group.


Reflection Questions

How does the Diamond Model help in understanding threat actors?	

The Diamond Model breaks cyber-attacks into four core parts: the Adversary, their Infrastructure, their Capabilities (tools), and the Victim. This helps analysts to see the connections between these elements. By understanding the links among these elements, they can better predict an attacker's future behavior. It also helps identify the attacker's goals and weaknesses. This makes it easier to defend against them effectively.

What challenges did you face in identifying each vertex?

Identifying the vertex and what they stand for were challenging because not all the names given to the vertex directly reflect what it means:

Adversary – this has a direct meaning as an attacker or enemy.
Capability – according to the Diamond Model Analysis, it refers to the tools and malware deployed by the attacker to achieve their aims.
Infrastructure – this refers to the technical assets used to conduct the operation. Assets like command and control servers, IP addresses, domains etc. Again, infrastructure does not directly interpret into what its name implies in terms of Diamond Model Analysis.
Victim – by this Model, victim includes Organizations, Windows Servers, and Industrial Control System Devices etc. While I easily understand why an organization can be a victim, It is challenging to see devices like Windows Servers as victims in the Model.

How could this model support proactive defense strategies?

The Diamond Model enables proactive defense by identifying patterns in adversary Infrastructure and Capabilities to block attacks before they start. It guides threat hunting by using known indicators to search for hidden attackers. By analyzing historical TTPs, it allows you to predict and guard against an adversary's next likely actions. This intelligence can also be used for infrastructure denial, proactively blocking malicious domains and servers across the network. Ultimately, it shifts the focus from reacting to alerts to systematically disrupting the adversary's entire attack lifecycle.

