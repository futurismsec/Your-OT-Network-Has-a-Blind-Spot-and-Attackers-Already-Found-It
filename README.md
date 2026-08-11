# Your-OT-Network-Has-a-Blind-Spot-and-Attackers-Already-Found-It
CISA and the FBI say cellular modems and exposed PLCs drove a multi-state wave of water utility attacks in 2026. Here's what happened and how to close the gap.

On July 30, 2026, CISA and the FBI issued an urgent joint alert describing a sharp escalation in attacks against internet-exposed programmable logic controllers (PLCs) across the Water and Wastewater Systems (WWS) sector. It's the kind of advisory that should stop every OT and industrial security team in their tracks  not because the attack technique is sophisticated, but because it isn't.

**What happened**
The wave started over the weekend of July 26–27, 2026, when more than 30 community water systems in Minnesota were hit in a coordinated round of intrusions. The activity didn't stay contained. Within days, Michigan and other states reported similar incidents, and the FBI confirmed affected utilities in at least seven states.
The mechanism was almost insultingly simple. Attackers found PLCs and HMIs that had been left reachable from the public internet often set up that way by a vendor, integrator, or field technician years earlier and then forgotten. Many were still running default or weak credentials. Once inside, the attackers didn't need to deploy exploits or malware. They just logged in, changed the passwords to lock operators out, and in some cases altered the device's IP address to sever it from the network entirely. Several utilities had to issue boil water notices and revert to manual operations while they scrambled to regain control of pumps, valves, and chemical dosing systems.
CISA's advisory specifically named equipment from three major automation vendors Rockwell Automation/Allen-Bradley, Siemens, and Schneider Electric as being affected. A later update noted something more concerning than the lockouts themselves: in some incidents, attackers exfiltrated PLC project files before leaving. That's not vandalism. Stealing the actual engineering logic that drives a treatment process is reconnaissance, and it suggests some of these actors are positioning for more targeted disruption down the road, not just quick, opportunistic mischief.

Why "mature" security programs got hit too

One detail in the advisory should concern every OT leader who assumes their perimeter is under control: CISA noted that organizations of all sizes were targeted, including utilities with established cybersecurity programs. The common thread wasn't a lack of investment in security it was a blind spot most attack-surface scans don't cover.
Specifically, CISA flagged cellular modems as a recurring entry point. These are often installed directly by a vendor or system integrator for remote support and diagnostics, outside the utility's normal IT change-management process. They rarely make it onto an asset inventory, they're invisible to network-based vulnerability scans, and they provide a direct, unmonitored path from the public cellular network straight into the OT environment. A security team can have firewalls, segmentation, and monitoring dialled in and still have a five-year-old modem quietly bridging the plant floor to the internet.

The advisory also connects to a longer-running problem: CVE-2021-22681, a critical Rockwell Automation vulnerability with a near-maximum severity score, sat unpatched for years because ICS environments are notoriously hard to patch without risking service disruption. Iranian-affiliated actors have been actively exploiting it since March 2026, and Rockwell has 
confirmed no patch is coming meaning network isolation and compensating controls aren't optional extras, they're the only real defense.

**What CISA is asking operators to do**

The advisory's core recommendations are not exotic, and that's precisely the point most of this incident chain was preventable with basic hygiene:
•	Remove PLCs, HMIs, and other OT assets from direct internet exposure. If remote access is genuinely required, it should go through a VPN with MFA, not a bare public IP.
•	Inventory every remote-access pathway into the OT network including cellular modems and anything installed by third-party vendors or integrators, not just what shows up in a standard network scan.
•	Change default credentials on every industrial device, and enforce strong, unique passwords going forward.
•	Build and test an isolation and manual-operations plan so a lockout event doesn't turn into an extended service disruption.
•	Watch for tampering in reusable code modules embedded in control logic and monitor for unauthorized project file access or exfiltration.
•	Report incidents promptly to CISA's 24/7 Operations Center or the FBI's IC3, so the broader sector benefits from shared indicators.

**The bigger picture**

This isn't a one-off event. It's a preview of what happens when decades of "we'll deal with OT security later" collides with attackers who have realized they don't need zero-days they just need a search engine and a default password. Water and wastewater utilities are attractive targets precisely because the consequences of disruption are immediate and physical: no water pressure, no verified chemical dosing, no confidence in what's coming out of the tap.

For any organization running PLCs, HMIs, or other OT/ICS equipment water utility or otherwise this advisory is worth treating as a mandate, not a headline to skim past. The gap between "we have a cybersecurity program" and "we actually know every path into our OT network" is exactly where these incidents lived.
If you're not confident you could answer, right now, exactly how many remote-access points exist into your OT environment  including the ones a vendor installed and never told you about  that's the question worth answering before an attacker answers it for you.

Need a clear-eyed assessment of your OT/ICS exposure? Futurism Security's OT/IoT Security Consulting team specializes in exactly this kind of gap analysis — mapping undocumented remote access, hardening PLC configurations, and building the isolation plans CISA is now urging every critical infrastructure operator to have in place.










