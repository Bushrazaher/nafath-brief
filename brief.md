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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
