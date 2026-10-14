Version: NAFATH-V4
Track: Software

## Overview
A national service provider depends on more than secure applications. Its services also rely on trustworthy software components, reliable AI models, secure mobile applications, accurate internet routing and well-managed data. A weakness in any one of these areas can affect the availability, confidentiality or integrity of the entire service. For example, a vulnerable software library could allow an attacker to compromise an application, while manipulated AI training data could lead to unreliable decisions. These risks are connected, so security cannot be handled by separate teams working in isolation. The provider should combine secure development practices, AI testing, mobile security verification, routing validation, vulnerability management and software component inventories. For our software track, this starts with storing configuration settings and secrets in environment variables rather than hardcoding them in the source code.

## Software
Programs need configuration data to work properly, including database credentials, API keys, and server locations. It is important to avoid hardcoding these values into your program's source code. If your code becomes public, other people could find these settings and use them for malicious purposes. The Twelve-Factor App methodology recommends storing all settings in environment variables outside the code, while keeping sensitive passwords and keys protected, restricted, and rotated regularly.

Resource: The Twelve-Factor App: Config - https://12factor.net/config

## AI
Adversarial attacks on machine learning systems include evasion, poisoning, and privacy attacks. Evasion occurs when attackers alter the data given to AI to produce incorrect results. Poisoning happens when attackers misuse data or add false information to the dataset used to train the AI. Privacy attacks aim to get private data from the training set or model responses. One happens when AI is used, one happens during learning, and one reveals private data.

Resource: NIST, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2023/final

## Mobile
The OWASP MASVS framework defines security requirements for protecting mobile applications. It groups requirements into specific levels: L1 for standard security, L2 for sensitive data such as banking apps, and R for resilience against reverse engineering. By combining this standard with the OWASP Mobile Application Security Testing Guide (MASTG), developers and testers can examine the application and verify data storage, encryption, and authentication security to fix bugs before deployment.

Resource: OWASP MASVS - https://mas.owasp.org/MASVS/

## Networking
BGP makes it possible for networks to inform each other about paths for sending traffic to specific Internet addresses. A network can announce that it delivers traffic to an address even when it is not authorized to do so, which is known as BGP route hijacking and sends traffic to the wrong network. With RPKI, networks validate if the entity announcing an address is authorized, though other checks and continuous monitoring are still required.

Resource: RIPE NCC, RPKI - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/

## Cybersecurity
Log4j is a Java tool that applications use to log events and errors. In December 2021, a major flaw called Log4Shell (CVE-2021-44228) was made public. An attacker could give data to an application to be logged and execute code on the affected system over the internet without logging in first. The primary method to fix the issue was updating to the fixed version, checking for vulnerable copies hidden in other applications, and confirming the fixes.

Resource: Apache Logging Services, Security - https://logging.apache.org/security.html

## Data
Organizations build applications using software components from many vendors. When a component has a security bug, an organization must know which applications use it. An SBOM (Software Bill of Materials) is like an ingredient list for a dish because it lists all parts of an application and how they connect. The minimum fields are supplier name, component name, component version, other unique identifiers, dependency relationships, SBOM author, and timestamp.

Resource: NTIA, The Minimum Elements for a Software Bill of Materials - https://www.ntia.gov/files/ntia/publications/sbom_minimum_elements_report.pdf
## Misconception in My Track
Many developers think that putting settings into separate config files for each stage, like dev.env or prod.env, follows the Twelve-Factor App rules. However, this is wrong because creating a new file for every test or developer environment quickly becomes messy and hard to manage. In the "Config" section of The Twelve-Factor App, the guide states that environment variables must be independent and managed separately for each deploy, never grouped together as named environments.

## Open Question
How can we update secret passwords inside running containers automatically when credentials change without restarting the whole application?

