![Banner](../images/banner.jpg)

in this first week we will understand the AI security landscape, build a basic AI system, and immediately break it to think like an attacker!

**day 01** will cover some theory aspects only 

in the first day i wanted to understand the difference between each sector when implementing AI because nowadays all feilds are witnessing a sort of race condition ! no company wants to be left behind, and AI is the key 

# Threat Profile: Finance Industry

**intro**
as the brain of economy AI advances in information processing, from double-entry bookkeeping to computers
Today, artificial intelligence represents the next major leap forward

**key application area**

we can see that AI is deployed across 4 critical financial functions i call it FAIP:
Financial Intermediation, Asset Management, Insurance, Payments & RegTech

### 1. Financial Intermediation
Connecting savers with borrowers; managing risk between parties.
- Credit scoring & loan underwriting
- Fraud detection
- Anti-money laundering (AML)
- Customer service chatbots

### 2. Asset Management
Managing investments and portfolios on behalf of clients.
- Algorithmic trading
- Robo-advisory (automated investment advice)
- Portfolio optimization
- Sentiment analysis (from news/social media)

### 3. Insurance
Risk assessment and compensating policyholders for losses.
- Underwriting automation
- Claims processing
- Fraud detection
- Personalized pricing

### 4. Payments & RegTech
Facilitating transactions and ensuring regulatory compliance.
- Real-time transaction monitoring
- Regulatory compliance automation
- KYC (Know Your Customer) screening
- Payment fraud prevention

## what attackers wants?**
this is the most interesting question right ? and the most obvious one, the WHY ?
attackers, attack AI for 4 main reasons : 

1. **Money (direct theft):** Steal funds via fraudulent transactions, deepfake social engineering, or manipulating trading algorithms 
2. **Data (PII & financial records):** Steal customer information, trading strategies, or proprietary ML models to sell or exploit.
3. **Systemic Disruption:** Crash markets, shut down platforms, or damage reputation to cause chaos.
4. **Espionage:** Steal competitive intelligence or national security data (especially nation states).


## who attacks ??
well your next question is obviously, who attacks ? 
i know that i talked about bad actors only like nation states, cyber criminals, insiders and competitors but also some heros (good people)
to beat a hacker , you should think like one or just get yourself a pentester witch a great knowledge about the field 

## Top threats 
### 1. Adversarial ML (Evasion & Poisoning)
in this one attackers manipulate transaction data to evade fraud detection, or inject poisoned data into training sets to corrupt credit scoring models.  
*Example:* fraudsters alter transaction amounts just below reporting thresholds to bypass AML algorithms
### 2. Insecure APIs & Cloud Misconfiguration
weakly secured APIs or exposed cloud storage lead to credential theft and data breaches aka the #1 cause of financial data leaks.  

*Example:* an exposed S3 bucket leaks millions of customer records
### 3. Deepfake & Identity Spoofing
we saw many many cases that used deep fake to steal data or even do worse ( well there's nothing worst than stealing data), so in here AI-generated voice/video impersonates executives to authorize fraudulent transactions or bypass biometric authentication.  

*Example:* a deepfake CEO voice calls a subordinate and authorizes a $10M wire transfer
### 4. Data Contamination
corrupting training or operational data pipelines to misallocate funds, distort risk assessments, or manipulate portfolio recommendations.  

*Example:* poisoned market data causes an algorithmic trading bot to make bad trades 
### 5. Third-Party & Systemic Risk
a compromised vendor (data provider, cloud service) or a cyber incident propagating through interconnected fintech ecosystems creates single points of failure. 

*Example:* a breach at a major cloud provider takes down multiple banks simultaneously
**golden advice :** a compromised vendor is a compromised company (this is a NAUR's quote, do not take it seriously)

# Threat Profile: Healthcare Industry

**intro**
Healthcare has always been data-intensive from paper charts to electronic health records (EHRs), today AI is transforming diagnosis, treatment, and hospital operations. But unlike finance, where the stakes are money, healthcare stakes are human lives!

The healthcare sector faces a unique convergence of challenges: the sensitivity of patient data, the life-critical nature of clinical decisions, and increasingly sophisticated cyberattacks, AI adoption has become "widespread at tremendous speed and scale," making security governance an urgent priority 

Cyber safety is patient safety 

```see how noble cyber security is ?```

## key application area
AI is deployed across four critical functions that i call (wait i hope you're not taking those random abreviations seriously) 

### 1. Diagnostics & Imaging

well AI can assists doctors in detecting diseases from medical images like: 

1. Radiology (X-ray, MRI, CT scan analysis)

2. Pathology (cancer cell detection)

3. Dermatology and ophthalmology screening

how cool!

### 2. Clinical Documentation & Decision Support

AI helps doctors spend less time on paperwork and more time with patients.

1. EHR summarization (condensing patient histories)

2. Clinical note generation (auto writing visit summaries)

3. Triage assistance (prioritizing urgent cases)

4. Multilingual patient communication (translating for non english speakers)

### Monitoring & Patient Care
AI watches over patients 24/7, something humans can't do.

1. Remote patient monitoring (wearables like smartwatches)

2. ICU early warning systems (predicting patient deterioration)

3. Chronic disease management (diabetes, heart failure)

4. fall detection for elderly patients

basically AI is the ultimate night shift worker (i can finally sleep, who lied to you?)

### Drug Discovery & Personalized Medicine
AI accelerates finding new treatments and matching them to specific patients.

1. Genomic analysis (understanding your DNA) ```this one is my fav```

2. Drug repurposing (finding new uses for existing drugs)

3. Clinical trial matching (finding the right patients for studies)

4. Treatment recommendation systems

## what Attackers Want
same 4 reasons as finance but with a healthcare twist
you know ransomeware payements are kinda higher cuz : 
to save lives faster <=> you pay higher

## who attacks
same actors as mentioned in the finance industry threat profile

## Top Threats
### 1. Data Poisoning of Diagnostic Models
attackers inject corrupted training data to make AI models consistently wrong
### 2. Adversarial Attacks on Medical Imaging
attackers add tiny changes to medical images that humans can't see but AI gets confused by.
*Example*: subtle noise added to a lung X-ray causes the AI to miss cancer detection, the image looks normal to doctors but AI says "all clear" when it shouldn't
### 3. Ransomware on Hospital Infrastructure
attackers encrypt hospital systems and demand payment, often hitting critical care (and then you should pay)
### 4. Patient Data Breaches
hackers steal PHI (Protected Health Information) to sell, commit fraud, or blackmail.
*Example*: a hacked EHR system exposes 50,000 patient records, including mental health histories, HIV status, and genetic data
### 5. AI Misdiagnosis Due to Model Drift
models get worse over time as patient populations change, without retraining obviously.
### 6. Agentic AI Attacks (The New Kid on the Block)
cybercriminals weaponize AI agents to carry out sophisticated attacks automatically.
*Example*: a threat actor used Claude (Anthropic's LLM) to extract data from 17 organizations including healthcare,using **vibe hacking** (interacting with the chatbot in real time during attacks)

a vibe hacker can be problematic sometimes, they don't just play ctfs trust me

# Threat Profile: Automotive Industry

Cars aren't just cars anymore, they're data centers on wheels! Modern vehicles have 100+ Electronic Control Units (ECUs), millions of lines of code, and are increasingly connected to the internet, cloud services, and each other 
Autonomous driving, connected car features, and AI-powered systems have turned the automotive industry into a prime target for cyberattacks
unlike finance (money) and healthcare (lives), automotive attacks can cause physical harm AND financial loss simultaneously (it combines both)

## Key Application Areas

### 1. Autonomous Driving (ADAS & ADS)

AI powers self-driving and driver-assistance features 

1. Lane keeping assist

2. Adaptive cruise control

3. Automatic emergency braking

4. Full self driving (FSD) capabilities

5. Automated Driving Systems (ADS) lvl 3 and higher 

### 2. Predictive Maintenance

AI predicts when parts will fail before they do

1. Engine health monitoring

2. Battery degradation prediction

3. Tire pressure and wear analysis

4. Brake system diagnostics

### 3. Connected Car Services

AI powers infotainment and connectivity features 

1. voice assistants (like Alexa in cars), vulnerable to prompt injection attacks 

2. Navigation and traffic prediction

3. OTA (Over-The-Air) software updates

4. Smartphone integration

### 4. V2X Communication (Vehicle-to-Everything)

AI enables cars to communicate with everything around them 

1. V2V: Car-to-car communication (avoiding collisions)

2. V2I: Car-to-infrastructure (traffic lights, road signs)

3. V2P: Car-to-pedestrian

4. V2N: Car-to-network (cloud updates)

### 5.Manufacturing & Supply Chain

AI optimizes production and logistics

1. Quality control (defect detection)

2. Robot automation

3. Supply chain optimization

## who Attacks?

same as other sectors but we will also have some new actors like : car thieves and terrorists, yes terrorists can weaponize those cars after all

## Top Threats

### 1. Remote Vehicle Takeover
Attackers exploit vulnerabilities to control critical vehicle systems remotely.

> **Real Incident:** Researchers hacked a Jeep Cherokee in 2015—remotely controlling AC, radio, windshield wipers, brakes, and steering

### 2. OTA Update Tampering
Attackers intercept or corrupt software updates to install malware.

*Example:* a malicious update pushes ransomware to millions of cars overnight

### 3. Sensor Spoofing
Attackers physically manipulate sensor inputs to fool AI decision-making.

*Example:* fake traffic signs cause autonomous cars to make dangerous decisions

### 4. V2X Spoofing
Attackers send fake signals to vehicles and infrastructure.

*Example:* a fake "emergency stop" broadcast causes a pile-up

### 5. Data Poisoning
Attackers manipulate training data used to build self-driving AI.

*Example:* poisoned training data makes self-driving cars consistently run stop signs

## Why AI Specifically?

AI systems operate at an unprecedented scale. They process enormous amounts of data, make critical decisions, and can perform actions far faster than humans can react. That's both the greatest strength of AI and one of its biggest security challenges.

### But why learn AI hacking?

I recently watched a video on this topic, and one idea really stuck with me: **AI hacking feels like the early days of web hacking.**

![Banner](../images/havij.jpg)

The field is still young, New vulnerabilities are being discovered, defenses are still evolving, and there's plenty of room for research and creativity. It feels fresh, exciting, and full of opportunities for anyone who enjoys exploring how systems work and how they can fail

For me, that's what makes AI security so interesting. We're witnessing the birth of a new security domain, much like web security was years ago

Anyway, I've talked enough for one report 

see you in the next one!

**happy AI hacking!** 🚀
