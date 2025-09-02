# h2 - Kill Chain

## Hutchins et al 2011

### Abstract

- Traditional network defense technologies (like intrusion detection systems and anti-virus) primarily deal with the vulnerability element of risk, and traditional incident response assumes the intrusion has already successfully happened.
- These traditional processes do not work well with complex threats, such as Advanced Persistent Threats (APTs), because of their different goals and sophistication.
- APTs are identified as very capable and well-resourced adversaries that can conduct campaigns of intrusion over years with the objective of stealing valuable and sensitive economic, proprietary or national security information using advanced tools and techniques that can circumvent most traditional defenses.
- To effectively disrupt APTs, we require an intelligence-based computer network defense (CND) model that addresses the threat side of risk, not only the vulnerabilities.
- This would involve:
  - Using what we know about adversaries to create an intelligence feedback loop.
  - Utilizing a kill chain model to describe the phases of intrusions.
  - Mapping adversary kill chain indicators to defender courses of action.
  - Linking individual intrusions to identify patterns of a larger campaign.
  - Recognizing the intelligence gathering is an iterative process.
- Institutionalizing this iterative intelligence-based model will provide defenders the opportunity to simultaneously reduce the chances of adversaries being successful, inform decisions on how to invest in a network defense, prioritize deployment of resources in a network defense, and facilitate relevant measurements of performance and effectiveness.

### Intrusion Kill Chain

- A "kill chain" is defined as a systematic means to find and attack an opponent in order to achieve a desired effect.
- Term is adapted from military doctrine to describe the lifecycle of a cyberattack.
- There are seven phases:
  - Reconnaissance
    - Adversary learns about the target (infrastructure or personnel).
      
  - Weaponization
    - Adversary packages exploit/code with a delivery mechanism (malware in document).
      
  - Delivery
    - Adversary sends exploit by email, web, or removable media.
      
  - Exploitation
    - The delivery mechanism is activated, exploiting a vulnerability or user action.
      
  - Installation
    - Malware installs a back door for persistent access.
      
  - Command & Control (C2)
    - Compromised system establishes a connection to the adversary for remote control.
      
  - Actions on Objectives
    - Adversary executes their mission (sabotage).

- Disrupting any phase severs the link and prevents the attack.
- Allows defenders to move away from reactive security, to proactive.
 
## Tactics, tools & procedures

### Tactics
Tactics define the “why” of an ATT&CK technique or sub-technique. It is the adversary’s tactical objective and the reason for completing one or more actions. An example of a tactic is execution and an adversary trying to run a malicious code to steal data.

### Techniques & sub-techniques
Techniques are “how” an adversary maneuvers in order to obtain a tactical goal by performing an action. Sub-techniques are a more precise description of the adversarial behavior to achieve a goal. They describe behavior in a lower level than a technique. 
An example of a technique is developing capabilities which means adversaries might develop and create their own tools and resources such as malware, exploits, or certificates instead of externally acquiring them. This encompasses the process of identifying the operational requirements, then building and creating custom capabilities. 
These developments can be used in many steps of the attack lifecycle.
And malware is an example of a sub-technique of developing capabilities. 
Adversaries may conduct their own development of malware and related components for use in targeting operations rather than relying on third-party sources. 
This development or build process may include payloads, droppers, backdoors (such as backdoored system images), packers, command-and-control (C2) protocols, and even infected removable media. 
Building as opposed to buying these tools provides attackers with control over their build, allows them the benefits of maintaining persistence on compromised systems, obfuscating detection mechanisms, and executing post-compromise actions with more effectiveness throughout the compromise.

### Procedure
Procedures refer to the specific way that the adversary implements a technique, or sub-technique. 
For example continuing with the example I gave in techniques, a procedure of a malware sub-technique could be a group which create malwares.

# References
- Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains, chapters Abstract, 3.2 Intrusion Kill Chain (https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)
- https://attack.mitre.org/resources/faq/#general-faq
- https://attack.mitre.org/tactics/TA0002/
- https://attack.mitre.org/techniques/T1587/
- https://attack.mitre.org/techniques/T1587/001/
