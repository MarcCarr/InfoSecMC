# Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains
(https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)

## Abstract 
- An evolution in network protection is required to counteract a more advanced method of attack - APT.
- APT's (Adnvanced Persistent Threat) are conducted by highly skilled individuals over a long period of time with the tools to bypass conventional network defences in order to gain access to essential systems and sensitive data.
- Defence actors can utilise the long-winded process to evaluate incoming threat techniques, and enhance mitigating actions for better success in future attacks.
- The kill chain model can be used to follow the bread crumbs of attackers to build a big picture view of their objectives.

## Introduction
- Succesful ATP attacks on highly classified entities proved a necessity to create more robust defensive measures compared to traditional blockades on automated attacks.
- An intelligence-driven approach is needed to combat sophisticated ATP attacks.
- The kill chain model represents each phase an attacker must go through to complete their objective succesfully, and preventing them in any one of the steps can greatly alleviate the probablity of success.

## Related Work
- Phase based defensive models are a common tool in developing and assesing counter measures.
- The US military forces apply a kill chain model for situational scenarios, and the US Department of Defence classifies their kill chain phase based model to include the steps: find, fix, track, target, engage, and assess.

## Intelligence-driven Computer Network Defense
- Intelligence-driven CND requires understanding of the adversary along with following the overall goal if intrusion attempts rather than focusing on one-time attacks.
- APT's are essentially defended with the same or higher level persistance.

## Indicators and the Indicator Life Cycle
- Indicators are an essential part in locating intrusions and harnessing them to locate more.
- Indicators are divided into three types:
 - Atomic - A basic form of data that retains its essence such as an IP address.
 - Computed - Genterated types of data such as hash values.
 - Behavioral - A combination of the two former types of data that an attacker utilises to further their objective.
- Indicators seem like a very small part of the defencive action, but they are a vital part in helping to build a adaptable strong defence in the long run.

## Intrusion Kill Chain
- Keyword "Chain" aptly describes this phase based model as failure in any one link will cause the whole process to cease.
- The intrusion kill chain includes seven steps:
 - Reconnaissance - Researching openly available infromation on target.
 - Weaponization - Create deliverable malware.
 - Delivery - Dispatch weapon to target with e.g. email attatchment.
 - Exploitation - Code triggers in target system attacking vulnerabilities.
 - Installation - Install means for remote access for steady control of in target system.
 - Command & control (C2) - Gain hands on keyboard access through an establsihed server connection.
 - Actions & Objectives - Fulfill original mission and extract data or move laterally within target system.
-As mentioned in the lesson, the final part of the kill chain is also the first part as you must have an objective before starting any other steps.

## Courses of Action
- Having a perceptive understanding of the adversary and their objectives allows for effective targeted defencive action.
- Each phase of the intrusion kill chain has a correlating phase in the courses of action matrix designed to promote resiliant defence versus persistant attack, and force adverseries to sink more cost into their objective.
  - Courses of action matrix consits of detect, deny, disrupt, degrade, deceive, and destroy.

## Intrusion Reconstruction
- Full understanding and abilty to reproduce a succesfully mitigated attack is an integral part of building a proactive defencive strategy for future intrusions.

## Campaign Analysis
- Campaign analysis is about studying long-term attacks and connecting the dots between similarities to get better insight on the adversary's intents and capabilities.
- Ananlysis can provide information on existing campaigns or open the door for investigation to a new campaign.

## Case Study
- Three similar intrusion attempts were made in a two-week period where attackers sent a weaponized attachment to a limited amount of individuals via email. The sending address was disguised as a legitimate employee to invoke authenticity.
- The attacker's objective was to install a backdoor from the attachment, and open a connection to a C2 server.
- The first two had many commonalities which defenders leveraged to thwart the intrusion.
- The third intrusion attempt differed from the first two, but was found out due to small similarities in key indicators.
- This case study is a testament to how effective careful analysis of each indicator and step of the intrusion kill chain can prove fruitful for network defence.

# a) Bookworm

I'm using a MacBook Air with an M1 processor, therefore I followed the instructions made by Teemu Laine https://github.com/HortTemppa/horttemppa.github.io/blob/main/h1.md

## Installation & Set up
- Instead of VirtualBox, I downloaded UTM virtualisation software here: https://mac.getutm.app/

- After downloading and confirming installation, UTM opened to this screen:

![Screenshot 2024-08-28 at 16 19 28](https://github.com/user-attachments/assets/672096d1-9953-4823-9b60-bcbd833f891d)

- I selected "Browse UTM Gallery" which opened the gallery in my browser.
- I picked Devian 12, and selected "Open in UTM". UTM asked to confirm the choise and installed Debian 12.
- Debin 12 was now visible on the left side where I right-clicked it to open the system preferences (Edit)
- In "Information" I set my own username and password. (These did not work on first log in)
- In "System" I increased the RAM to 4GB pictured below.
- Resizing over 4GB resulted in the VM not working!

![Screenshot 2024-08-31 at 23 19 03](https://github.com/user-attachments/assets/e33fdfa9-be46-497e-9186-99f0fac12bfb)

- In "Network" I switched Network mode to "Bridged"

- Finally I clicked save and pressed play on the virtual machine.
- Boot process was quite long, patience is needed.
- After boot, I logged in with default username and password.
- I opened "Activities" -> "Settings" -> "Users", and changed username and password to my own.

![Screenshot 2024-08-31 at 23 06 38](https://github.com/user-attachments/assets/eec2c45d-adcf-4074-ba7f-4b7c2cfc29c1)

## a)
- I opened the terminal and used "sudo apt-get update" to update available software.
![Screenshot 2024-08-31 at 23 11 37](https://github.com/user-attachments/assets/f5bd4b94-ad32-4450-b1c3-b629fa1a13b3)

Some thoughts after completing this partly:
- UTM VM is painfully slow with Mac M1 (at least mine)
- I had to reinstall UTM / Debian at least 5 times before it worked at some capacity.
- Debian download time varied from up to 6h to 15 minutes.
- VM uses a huge amount of CPU, and usage is not stable.
- VM crashed a lot or simply stopped responding.







