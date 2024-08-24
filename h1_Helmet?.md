# X - Threat Modeling Manifesto

The Threat Modeling Manifesto is a set of guidelines and questions helping you to determin how to threat model. Along with guidelines, the manifesto introduces a collection of principles and values that the authors follow when creating a threat model. The manifesto establishes four questions you should answer when threat modelling:

1. What are we working on?
2. What can go wrong?
3. What are we going to do about it?
4. Did we do a good enough job?

- The threat modeling process seems simple, but the four questions force you to truly look at what you have and plan accordingly.

## X - Shostack 2022: Welcome to the Worlds Shortest Threat Modeling Course (https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf)

- In his 12-part course, Adam clearly and concisely describes what threat modeling is and covers the 4 key questions you need for effective threat modeling.

- Adam introduces tools such as sketching, diagramming, documentation and collaboration to enhance the understanding improve your threat modeling. Another effective tool is the STRIDE method which can be used to create a broad scope for your threat model.

- Once the question of "what can go wrong?" has been answered, a course of action must be decided for their prevention. An assessment for each threat-action combination has to be done and a deployment decision made. Finally, Adam stresses the importance of evaluating the work for future threat models.

- When creating a threat model, it's important to remember there will be a lot of eyes on the final product therefore you must create a model which is coherent and concise.

## OWASP CheatSheets Series Team 2021
- OWASP’s cheat sheet introduces threat modeling as an integral part of the SDLC (software development life cycle) where the designers focus on the perspective of an attacker.
- Threat modeling allows for a proactive safety strategy rather than reactive, which also allows for greater insight on the protected system.
- OWASP divides the threat modeling process into four steps:

System modeling
- Building a full scale understanding of the system, and associated entities with the help of visual materials and collaborative efforts.

Threat Identification
- OWASP focus on the STRIDE (Spoofing, Tampering, Repudation, Information Disclosure, Denial of Service, Elevation of Privileges) technique, which effectively forces threat modlers to consider a wide array of possible attacks.

Response and Mitigations
- OWASP borrows Adam Shostack's META (Mitigate, Eliminate, Transfer, Accept) method for choosing the correct response to a threat.

Review and Validation
- The final step is for all associated parties to critically review the threat modeling process.

- Although the four steps are very closly to related to the threat modeling Manifesto's four questions, they give a slightly different perspective which anchors in the fact that there is no "right way" to threat model.

## The Darknet Diaries - Ep. 75 Compromised Comms

Compromised Comms introduces the story of one of the biggest security breaches in modern espionage. The story begins between 2009 and 2011 when Iranian officials discovered that the US had uncovered a lot of information about their enrichment efforts. Iranian officials suspected they had a mole once they found a malicious computer worm, Stuxnet, which had damaged Iran's nuclear program. Stuxnet is a physical piece of malware, which means it had to be walked into a top-secret Iranian facility, hence why Iran suspected a mole. Iran and the US are considered adversaries, therefore the US doesn't have any diplomatic status in Iran. This made it far more difficult for Iranian intelligence to locate possible spies. The CIA had a network of agents, assets, sources and handlers in and around Iran. One of them happened to be a double agent for the Iranian intelligence organisation. The double agent had found one source of communication that the CIA was using to contact these assets.

The CIA, at the time, was using dummy websites about mundane everyday stuff such as excercise or fishing. Websites that looked innocent and wouldn't raise any suspicion. These websites had a specific pixel at a specific time (most likely) that an asset could click to log in and open a line of communication directly to the CIA, where information could be exchanged and meetings set up. The Iranian intelligence organisation hacked into the first website the double agent had provided for them, and they realised there was little to no encryption for the communication line. After uncovering how the website worked, they found every other similar website as they shared commonalities.

Iran had full access to all CIA communication in their area, and they eventually started breaking apart the network by making arrests and killing assets. The situation got even worse for the CIA because Iran started to very openly share this intelligence with their allies, most notably China. The CIA had a large-scale operation going on in China at the time as well, and they were using the same method of communication. China began eradicating CIA assets quickly after receiving the intelligence from Iran and an estimated 70% of CIA operations was destroyed in China and it hasn't bounced back since.

The US are still yet to publically make a statement or comment about this disaster in covert communication. Reporter Jenna McLaughlin estimates this affected dozens of CIA operatives and closer to 100 people in all. Most of whom were imprisoned or executed. This whole fiasco could have been avoided if the CIA had listened to John Reedy. John was a whistleblower who worked as a targeter for a contracting company and he brought up the major issue with this line of communication to the CIA already in 2009. Unfortunately for the CIA and everybody involved, he was ignored.

- Why would the most powerful intelligence organisation in the world use an open source communication line when it is paramount that the line is completely airtight?
- Is it possible to have a 100% secure line today between adversarial countries?

## a) Security hygiene

There are many basic things everyone should do to stay secure in today's online world.

Password management:
- Don't give out your passwords
- Avoid using the same passwords on multiple services
- Avoid using similar structure for all your passwords
- Keep passwords seperate from usernames or preferably memorize them / use password manager

Common sense:
- Don't give out any personal information to an unverified source
- Utilise protective services (Antivirus, adblock, VPN)
- Be mindful of what sites you visit
- Don't click links willy nilly

## b) Make-belief boogie-man
My company is a quaint clothing brand specializing in creating hand-made clothes. A base range of classic lines along with custom requests from clients. The business operates mostly online, and there is a boutique along with a warehouse for shipments. Employees include: Owners, designers, tailors, graphic designers, social media managers, retail workers, customer service reps, marketing, 

What are we working on?
- Building brand recognition
- Customer trust - Keep customer information secure
- New designs
- Usable secure website
- Clear and easy deliveries
- Welcoming store

What can go wrong?
- S = An attacker can send an email to an employee pretending to be someone else to attempt to gain access to the company's system. 
- T = An attacker can get access to the supply chain and tamper with finished products or fabrics resulting in a loss in revenue as well as trust.
- R = A customer can claim to have not received their order after it has been sent.
- I = An attacker can gain access the company's employee data where personal information and financial records are stored.
- D = The company website can be overloaded, which will deny access for customer's to access it.
- E = An attacker can gain access to admin rights on the website or social media where they can show what they want.

These are just singular examples of possible attacks this company could suffer, and there are numerous other ones. The biggest priorities for this company are:
- Customer data
- Secure suplly line
- Brand image

Suffering a succeful attack for any of the three above could be disasterous for the company. Realistically, a small scale clothing company won't have specific actors attempting attacks. Most probable would be a rivaling brand or coincidental physical attacks on supply chain. 

What are we going to do about it?
- Customer data must be locked down securly
- Suplly line must be trusted and secured
 - Data for both can be protected with robust server security along with employee training.
 - Fabrics an shipments require trusted partners.

- Payment details can be set up with a third party to mitigate risk.
- Deliveries go through third party partners where risk for package loss has to be accepted with the partner.
  - Step-by-step tracking can mitigate losses.

- Website must be carefully created to not leave backdoors for potential attackers.
- Social media must be carefully monitored and kept strictly in-house.
- Brand affiliate's have to be picked carefully with brand image in mind.

Did we do a good enough job?
- Threat model must be updated and adjusted as we go.
- Employee training is constant - E.g. dummy phising tests periodically.
- Outside testing can be considered. E.g Social engineering, system hacking.
- Get input from partners and customers. Outside insight can be invaluable.
