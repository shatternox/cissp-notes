
## Domain 1 - Security and Risk Management

**CIA Triad**
![[Pasted image 20240903233256.png]]

**Confidentiality**
![[Pasted image 20240903233454.png]]
--> Nowadays,  it's hard to break encryption unless there's a side-channel attack possibility.
--> Need-to-know (You only have access on what you need to know, don't give too much access or information)

**Integrity**
![[Pasted image 20240903234107.png]]
--> Integrity and Confidentiality are closely tied. If one weak, the other is also weak.
	- Even if we keep our data confidential but unauthorized people can change it, well it's not a viable data anymore.
	- If we have a great integrity but the confidentiality is breached, well the integrity might not matter either.

**Availability**
![[Pasted image 20240903235743.png]]
--> Data worth $10.000, kita punya cash $10.000. Gk mungkin kita abisin semua duitnya buat availability data tersebut. Gk worth. Kita harus mikir solusi efektif yang cost effective. That's why SLAnya gk harus 100%, boleh 99.9% to reduce the cost.
--> IPS gk boleh langsung dideploy, bisa false-positive dan block legitimate traffic. Makannya harus do a lot of tweaking dulu sebelum deploy IPS.
--> **When a Patch is out, attacker know there's a vulnerability**. There for gotta patch ASAP. Tapi, check dulu, compatible gk, apa yang harus diubah, dll. After all good, baru patch. Tapi jgn nunggu terlalu lama juga like 2 months.

**RPE (Resume Producing Event)**
--> 2 UPS (Uninterruptible Power Supply), masing-masing 60% load. 1 Orang gk sengaja matiin 1, jadinya loadnya pindah semua ke 1 UPS dan dia jadi handle 120% load. Sebagai safety mechanismnya dia jadi mati sendiri. In the end semua mati.

**RAID**
--> Duplicate HDD, realtime backup.

CIA Triad harus dibalance sesuai kebutuhan.
	- Too much Confidentiality and the Availability can suffer (kebanyakan jagaannya, mau akses jadi susah). "***If confidentiality measures are too stringent, it could impede the timely and unobstructed access to data by authorized users, thereby compromising availability***."
	- Too much Integrity and the Availability can suffer (sama juga).
	- Too much Availability and both the Confidentiality and Integrity can suffer.

Opposite of CIA Triad. The DAD Triad (**Disclosure, Alteration, and Destruction**).
![[Pasted image 20240904001235.png]]
**Disclosure** --> Someone not authorized getting access to your information.
**Alteration** --> Your data has been changed.
**Destruction** --> Your data or system have been destroyed or rendered inaccessible.

Pas Exam, CIA Triad gk akan ditanya definisi, tapi lebih ke scenario dan susah. Jadi harus bener-bener paham.


**IAAA (Identification, Authentication, Authorization, and Accountability)**
![[Pasted image 20240908102637.png]]

**MFA**
--> Something you know, **password**, **pin**, etc.
--> Something you have, **ID card**, **passport**, **smart card**, **browser cookie**, etc. 
--> Something you are, **biometrics**, **fingerprint**. 

![[{D0CA7143-C283-46E1-AED9-187EABDF6DB2}.png]]
**Authorization** --> Access Control, IDOR, BOLA, RBAC
**Accountability** --> Non Repudiation. Bukti kalau seseorang melakukan sesuatu.

CISSP itu bukan soal absolute security. Tapi soal what best decision at that situation for the business.

![[{5C543AF8-DE8F-462A-881C-3007C610BC4D}.png]]

**Security Governance Principle.** 
![[{9A7BA0BD-BE3A-420D-84A9-D99D5FF9F155}.png]]
**Least Privilege and Need to Know** --> Penting
**Non-Repudiation** --> Logging tuh bagian dari ini. 

Pas exam itu bakal scenario, dan kita harus pilih jawaban **yang paling benar**. Bisa ada 2 jawaban. Tetapi ntar **ada 2 distraction answer juga**.

**Digital Signature will provide Non-repudiation.**

======================================

**Management vs Governance**
![[Pasted image 20240909110517.png]]

--> Pas Exam, jawab dari POV yang exam mau (IT Security Manager / Risk Manager), bukan dari POV yang lu used to.

![[Pasted image 20240909111210.png]]
**Bottom-Up** --> IT Security is a nuisance. Tapi akan berubah ketika ada breach
**Top-Down** --> Management dan BOD, support IT Security. (approach pas exam akan gini)

CISO biasanya di bawah CTO, TAPI, **pas exam CISO di bawah CEO** langsung.

CFO --> Chief Financial Officer. Important.

### Governance Standards and Control Frameworks (Penting)
![[Pasted image 20240909111805.png]]
PCI-DSS --> Credit Card (Ada agar Credit Card tidak diregulasi Government. If we are good enough to regulate it, there's no need for government touch)
OCTAVE --> Self Directed Risk Management

COBIT --> Gold for the IT Organization. **Take what stakeholder needs and map it to our IT-related goals**. Have four domains.
1. Plan and Organize
2. Acquire and Implement
3. Deliver and Support
4. Monitor and Evaluate

COSO --> Goals for **ENTIRE** organization. COBIT was developed from COSO, tapi dibikin specific for the IT Organization.

ITIL --> IT Service Management. Set of frameworks and best practices that we use to align our IT services with the business' needs.

FRAP --> Specific. One business unit, application, and system at a time.
Roundtable brainstorm with **internal** employees. Impact analyzed, threats and risks are prioritized. Harus ada leadernya yang capable.

**ISO 27000 Series**
![[Pasted image 20240909123022.png]]

**Defense in Depth**
![[Pasted image 20240909123139.png]]

### Legal and Regulatory Issues
![[Pasted image 20240909124422.png]]
**Bakal keluar exam:**
- Criminal Law
- Civil Law (Tort Law) --> Financial Fines
- Administrative Law (Regilatory Law) --> HIPAA
- Private Regulations --> PCI-DSS

**Cuktau aja (Penting terutama di Indonesia):**
Customary Law
Religious Law

![[Pasted image 20240909144421.png]]
Liability:
- Kalau kita memang bertanggung jawab misalnya untuk mensecure website dan terhack, kita liable. Kalau kita udah DD dan saran ke senior management, tapi mereka gk approve, dan terhack, mereka liable.

Due Diligence (DD):
- Researchnya before we implmenet something, proses checkingnya. How are we going to fix things.
- ex: Prepare buat audit, pastikan semua sudah terimplemen dengan baik dan resource seperti uang dan waktu tersedia.

Due Care (DC):
- Implementasi hasil dari due diligencenya. Fixing the stuff.
- ex: Actual auditnya

Negligence (Lalai, tidak peduli, mengignore) --> Kalo kita mengignore risk yang tanggung jawab kita brati kita negligence dan bakal held liable.

**Evidence**
![[Pasted image 20240909145105.png]]
Real Evidence -->  Fisiknya, HDD, USB, Server, dll. We can touch it.
Direc Evidence --> They saw it, they experience it.
Circumstantial Evidence --> To support other evidence. ex: Witness. Mobilnya penyok.
Corroborative Evidence --> Not facts but can support other fact / evidence (?)

**Hearsay**
![[Pasted image 20240909154726.png]]

**Evidence Type**
![[Pasted image 20240909154802.png]]
Secondary Evidence --> Hearsay

**Reasonable Searches**
![[Pasted image 20240909160956.png]]
--> By default unreasonable search and seizure itu illegal by the US Government. **UNLESS, there's an immediate threat to human life or of evidence destruction.** In normal situation, harus ada search warrant.

**Entrapment and Enticement**
![[{8DEED465-EF4E-4093-AA03-D821BD005BDA}.png]]
**Entrapment** --> Menjebak orang.
**Enticement** --> Dia emng udh niat mau jahat, terus kita pancing lagi. Ex: Orang mau hack bank, kita sebagai admin sengaja buka port 22 tapi itu honeypot, supaya dia semakin napsu.

**Intellectual Property**
![[{326E7F91-F265-4934-BB3E-C30AC4F334F0}.png]]
**Copyright** --> Kita gk harus apply. Automatically granted. Cara jagainnya pake watermark.
**Trademarks** --> Kalo kita dah apply, kita bisa nuntut kalo ada orang yang berusaha make trademarks kita. e.g. for fake products, etc.
**Patents** --> Cryptograpic algorithm can be patents. Kyk punya Sam.
**Trade Secrets** --> Kalo dicuri gk ada legal backing. 

**Attacks on IP**
![[{339A2D3F-0272-40D8-83C6-85061DCC71E0}.png]]
**Copyright, Trademarks, and Patents** kalo dipake tanpa izin bisa company tuntut, for money.

**Cyber Squatting** --> Kalo dia sengaja beli domain yang tau kita akan pake buat ransom or hal jahat, or menjelek-jelekkan kita or seseorang itu **illegal**. Kalo krn kebetulan butuh yg sama, sah-sah aja.

**Typo Squatting** --> Beli domain yg mirip dengan domain aslinya. Mostly illegal krn dipake for phishing biasanya. Depends dipake buat apa.

Nerapin security controls itu harus mengacu pada business criticalitynya. Harus dari Highest business impact to lowest.

**Privacy**
![[{9FAAB99F-D999-4CC1-B7A0-E3CFE1AD3D7F}.png]]
**Kita sebagai konsumen ataupun warga negara BERHAK untuk PII kita itu dirahasiakan / disimpan dengan baik dan aman.**

EU Law paling bener buat privasi dan PII. 

PII --> Segala data apapun yang bisa merujuk ke seseorang. Even credit card number, biometrics, fullname, license, dll.

#### **Rules, Regulations, and Laws you should know for the exam (US)**
![[Pasted image 20240910104721.png]]
![[Pasted image 20240910105548.png]]
**HIPAA** --> for Health Insurance, Providers, Clearance House Agent.
HIPAA has three rules: a **privacy rule, security rule, and breach notification rule**.

**Privacy** - it is your right that your protected health information is kept private.
**The security rule** - they have to implement appropriate security measures.
**breach notification rule** - If they are breached, they need to let the public know.

**Security Breach Notificaitons Law** --> Harus ngabarin ketika breach. Tapi kadang kalau data yang breached/leaked itu encrypted with a strong encryption, mereka gk ngabarin.

**Electronic Communication Privacy Act (ECPA)** --> Old, protects against wiretapping.

**PATRIOT Act of 2001** --> Drastically improves ECPA.

**Computer Fraud and Abuse Act (CFAA) - Title 18 Section 1030** --> Cyber crime / Computer Crime paling banyak diarahkan ke sini. Karena mostly dipake buat Fraud.

**Gramm-Leach-Billey Act (GLBA)** --> Financial Institution.

**Sarbanes-Oxley Act of 2002 (SOX)** --> Accounting Scandals.

**PCI-DSS** --> Credit Card

#### **Rules, Regulations, and Laws you should know for the exam (EU)**
![[Pasted image 20240910105808.png]]
**General Data Protection Regulation (GDPR)** --> EU, Privacy, Fines.
--> EU Privacy law is the best, krn proactive.
--> Gk peduli lokasi perusahaannya, **KALAU customer kita ada yang dari EU, brati kita harus adhere to GDPR**.
--> Kalo customernya orang EU tapi gk stay di EU, gk harus comply.
--> Sangat agresif untuk mengejar company yg gk comply and besar finesnya. **Up to 20 Millios euro or 4% dari company revenue, which ever is greater**. Gila.

![[Pasted image 20240910110401.png]]
Data subject --> one of the individuals in the EU. Datanya gk boleh diproses unless ada legal basis to do so.

**Harus ada some sort of randomization ketika memproses data sehingga even kalo usernya agree, bakal susah diidentify.**

![[Pasted image 20240910110609.png]]
Kalo ada **lawful interception, national security, military, police, justice system yang minta. Then and only then baru boleh datanya di unmasked**.

Baca aja.

**Sebagai perusahaan, cuma boleh collect data that we only needs**. Gk boleh lebih.

**Company yang memproses dan monitoring data harus appoint/hire Data Protection Officers!**

**Legacy EU Laws (Predecessor of GDPR, no longer used)**
![[Pasted image 20240910111111.png]]

#### **Rules, Regulations, and Laws you should know for the exam (International)**
![[Pasted image 20240910131033.png]]
**OECD** --> Guidelines, for protection and privacy and transborder flows of personal data.

1. **Collection limitation principle** --> the collection of personal data should be limited,
2. **Data quality principle** --> data should be complete, current and relevant for what it is being used for
3. **Purpose specification principle** --> subjects need to be told why the data is being collected, the time that it is being collected, and that they only use it for whatever that purpose is.
4. **Use limitation principle** --> states that only with the consent of the subject or by the authority of law can personal data be disclosed, made available or used for anything else other than what it was intended for.
5. **Security safeguards principle** --> there should be reasonable safeguards in place to protect the data from loss, unauthorized access, modifications or disclosure.
6. **Openness principle** --> any practices and policies in regards to the personal data has to be communicated openly, and then the subject should be able to easily establish the existence and nature of the personal data, its use, and the identity of the organization that has the data.
7. **Individual participation principle** --> you should be able to find out which organizations have your data to make sure that you can correct any of the data that is wrong and be able to challenge any requests that are denied.
8. **Accountability principle** -->  organizations are held accountable for complying with the measures that are stated in the other seven principles.

**Wassenaar Arrangement** (Encryption, must have a good encryption)
![[Pasted image 20240910131744.png]]

PCI-DSS demands regular VA and Pentest

"The first principle of the General Data Protection Regulation (GDPR) is '**Lawfulness**, **fairness** and **transparency**'.

**3rd Party**
![[Pasted image 20240910132307.png]]
More aggressive the plan, more expensive it is.

Before acquisitions, kita mesti assess dulu security standard mereka. Kalo gk on par sama our current security standard, jadiin separate entity aja.

## **Ethics (PENTING BUAT EXAM)**
![[Pasted image 20240910132649.png]]
Kalo kita gk comply to Code of Ethicsnya, certifications kita akan direvoke.

![[Pasted image 20240910132846.png]]

**(Keluar di exam)**
![[Pasted image 20240910132935.png]]

### Information Security Governance
![[Pasted image 20240910133312.png]]
Setelah tau Values, Vision, dan Mission, baru kita bisa mikir strategic objectives dan actionsnya buat mencapai mission kita.

**Strategic Objectives**
![[Pasted image 20240910143539.png]]
**Strategic Plan** --> CEO, BOD, Higher management
**Tactical Plan** --> Kita di sini mostlikely, plannya lebih specific dan short term. Hiring, budgeting, training.
**Operational Plan** --> Lebih detail dan spesific lagi on what to do on operational.


**Policies, Standard, and Procedures (IMPORTANT FOR EXAM)**
![[Pasted image 20240910151958.png]]

**Policies are very high level.**
And for the IT world, for us, that could mean patches, updates, strong encryption. But there's nothing specific.

They're not specific and they fall into three categories.
- **Regulatory**, rumah sakit harus comply ke HIPAA, perusahaan yang ada user EU harus comply ke GDPR, Bank harus PCI-DSS comply, etc. 
- **Advisory**, the ones that outline what types of behaviors and activities that are either acceptable or not acceptable in our organization. In those types of policies, we would probably have some wording saying, *this is what happens if you do or do not follow the policy*. That could be our print policy, our acceptable use of Internet policy or our employment policies. We want our staff to clearly understand what is allowed and what is not allowed.
- **Informational,** the ones that are just there to inform people. That could be a policy that talks about our values, our vision, our mission.

**Standards (Mandatory)** --> Lebih detail dan specific.

*True policies and standards are more important, but maybe look at it a little bit more as we use our policies to build our standards. Then with those standards, we can find the guidelines and through those guidelines we can make our procedures*.

**Guideline (Non Mandatory)** --> Suggestion on how to implement it

**Baselines (Benchmarks)** --> Minimum requirements

**Procedures (Mandatory)** --> Low level, step by step guide to follow. Specific.

If we can automate something, do it, so we dont fuck up.

**Personnel Security (Human Aspect)**
![[Pasted image 20240910153826.png]]
Training dan practice lebih effective. Rather than seminar, mending gamification, **reward systems**, incentives, phishing simulation. It's better.

Human harus terus-menerus ditraining, gk bisa sekali aja. Harus dibiasakan, dan dijadikan habit.

**Background check** --> IMPORTANT, harus bener terutama buat remote employee, deepfake op. Inget kejadian Stepico. NDA juga.

**Employee Termination / Offboarding** --> Harus secure, hati-hati ada revenge attack. Access harus diremove semua dengan hati-hati. Shut off the access. **Remember, LOCK THE ACCOUNT, but never delete it**. We might need it for something in the future.

**Vendor, Contractor, and Consultant Security**
![[Pasted image 20240910155752.png]]
Vendor dan Outsource harus check. Hati-hati mereka leak informations.  

### Access Controls
![[Pasted image 20240910160220.png]]
**Administrative (Directive Controls)** --> **Hiring (background check) and Firing people juga include ke sini**.
**Technical Control** --> Logical Controls, firewall controls, how do we authenticate our staff, encryptions, etc.
**Physical Controls** --> Gates, guards, access card, locks, bollards, mantrap, etc.

#### **Access Control Types (SUSAH DAN KELUAR DI EXAM)**
![[Pasted image 20240910160512.png]]
Baca pertanyaannya bener-bener. Sesuain dengan situasinya. Karena even security guards bisa jadi Deterrent, bisa jadi Detective, or Compensating, etc. Gk ada yg selalu fixed.

DAN Pas exam bahasnya bisa beda. Bisa jadi Preventative, tapi ditulisnya Blocking. Asal meaningnya sama gpp. That's why this is an english exam.

*Also, keep in mind, this is an English exam. You might read through the entire question and all the options and you know, the answer should be something preventative. But they might use stop, or block, or avert and they may do that multiple times in a question you need to boil down, what are they exactly asking here? Even if the verbiage is not what you would expect, then you do the same with the answer options.*

**Detective controls** --> Log, logging juga termasuk.
**Corrective** --> Stop an attack or fix a problem. (antivirus, patches). 
- Khusus buat **patches, kalo Corrective gk ada di pilihan jawaban, PILIH Preventative**.

**Deterrent** --> Makes an attack less interesting, or less feasable.

**Compensating** --> Compensate kalo controlsnya impossible to implement. or too costly to implement.

### Risk Management - Identificaiton
![[Pasted image 20240910161350.png]]
**Risk = Threat * Vulnerability**
- If there's a threat tapi no vulnerability, then there's no risk.
- If there's a vulnerability but no threat, then there's no risk.
- Both needs to be present.

Risk Assessment itu process yang terus-menerus dan continuous.

*What is in scope is just as important as what is out of scope.* 
*What we're doing this risk assessment for? Is it for a single department? Is it*
*the entire enterprise? What type of assets are we looking at? What type of threats?*

**Rate yang paling critical dan paling likely diserang.**

### Risk Management - Assessment
![[Pasted image 20240910162605.png]]

*We have identified the risks and now we do our qualitative and quantitative risk analysis.*
*We do our risk register. And then we probably also do an uncertainty analysis, because even with the quantitative risk analysis, everything that we do here is really just our best guesses. We guess if this happens, then this is how bad it's going to be.*

Kita bikin risk, kasih risknya ke senior management, then, it depends on them whether to act on it or not.

After you put in a countermeasure, whatever risk is left over is the ***residual risk***. If that risk is still above our risk appetite, well, then we would do something else to either ***mitigate, transfer, accept, or avoid that risk***, which then brings us to risk transference. That is us transferring the risk to someone else.

**Risk Mitigation** --> Dibenerin.
**Transferring Risk** --> Insurance, Sharing risk (pake thirdparty partner).
**Risk Acceptance** --> Kita udah check semua dan kalo gk worth, yodah terima aja.
**Risk Avoidance** --> Stop whatever that's causing the risk. Matiin featurenya, etc.

**Risk Rejection** --> NEVER AN OKAY OPTION. Kita tau the risk is there, but choose to ignore it tanpa adanya analisa.

#### Risk Analysis
![[Pasted image 20240910163432.png]]
![[Pasted image 20240910163559.png]]
If the residual risk is still to high, we keep going.

![[Pasted image 20240910163656.png]]

PHI --> Protected Health Information --> is any health information that includes any of the 18 elements identified by HIPAA

![[Pasted image 20240910163841.png]]

We do the qualitative analysis, to make sure that we work on the right things, the ones that are important. 

We do the quantitative analysis to make sure we have enough protection for those things that are important.

![[Pasted image 20240910164054.png]]
 Quantitative Risk Analysis Example.
 ![[Pasted image 20240910164211.png]]
![[Pasted image 20240910164438.png]]

--> NONTON LAGI, INI NGITUNGNYA HARUS NGERTI. (Risk Management- Assessment Part 2)

![[Pasted image 20240910164851.png]]
![[Pasted image 20240910165036.png]]

#### KGIs, KPIs, and KRIs (Penting for exam)
![[Pasted image 20240910165208.png]]
**KGI** --> How well did we do compared to what we planned to do? Semacem kyk review. What went wrong, what can be improved (kalo gk mencapai target). Kuncinya adalah *after the fact*.

**KPI** --> Measuring how well we are doing in one specific task and it has a direct correlation between the goals and the performance.

**KRI** -->  Quantify and demonstrate the risks that the organization could be facing or how risky a certain activity is. Also used as an early warning system against risk.


## Risk Management 
![[Pasted image 20240923131444.png]]

At this point, we have identified the risks, we have presented our assessments to senior management, now they get to choose how we respond.

And remember, the only acceptable choices here are:
- risk mitigation, 
- risk transference, 
- risk acceptance or 
- risk avoidance.

And what I'm hinting at here is **risk rejection is never OK**.

![[Pasted image 20240924091444.png]]

**Risk Management Maturity Model**
![[{1BE52B35-6C8C-429E-A7F7-2DDF0479C89E}.png]]

### RACI (Responsible, Accountable, Consulted, Informed)
![[{B5BA65CC-DBAB-43C9-A41C-A25C4A5EA254}.png]]
**Responsible** **(R)** --> Yang tanggung jawab nyelesain tasknya. Someone that's doing the work. Kyk staffnya.
**Accountable** **(A)**  --> Yang merintah, yang approve or reject the work result. Kyk managernya.
**Consulted (C)** --> Yang ngasih input sebelum kita bisa membuat decision. SME. Komunikasinya harus two way, harus dialog
**Informed (I)** --> Orang yang harus diinfo terus mengenai progress. Komunikasinya searah aja, dari manager ke CISO misalnya. Just send them to the progress report.

**RACI Chart Example**
![[Pasted image 20241001234310.png]]


# GRC - Governance, Risk Management, Compliance
![[Pasted image 20241001234552.png]]

The governance structure of our organization is the one that establishes our ethical, legal and procedural guidelines for all the activities we do within our organization, including compliance.

## NIST 800-53 rev. 5 - Security and Privacy Controls for Information Systems and Organizations.

![[Pasted image 20241002000329.png]]
**492 Pages**
On the exam, there won't be a, "What is NIST 800-53 revision 5, control number SA-1?" **What you need to know is the high-level of the publication and then the usual why, when, where, how, what.**

**What is NIST 800-53 rev. 5?**
It presents us with a set of detailed security and privacy controls that primarily is intended for US federal systems, excluding the ones that are related to national security.

![[{CE63F041-9979-47DE-8D8A-E0686973A32C}.png]]
--> Baseline, bare minimum.

What's new in rev. 5
![[{972E6A65-D3A5-4524-A87B-21FC3AB121B7}.png]]
--> Thirdparty and supply chain risk management
--> Insider threat.

## NIST 800-37 Rev. 1 and 2

![[{B2CA11D2-67B4-4CAE-BC25-3FA04C6C3582}.png]]
**NIST 800-53 and NIST 800-37 is closely tied together.**

![[{B6B1D38B-7757-472F-9218-17DF5E19105F}.png]]

*"We implement security throughout the entire lifecycle of any system or software, meaning security and privacy are requirements in the initial design and all the specifications we need for a certain piece of software. And when I say the entire lifecycle, that means from when we acquire the software **all the way until it is completely removed from all our systems.**"*

![[{BC5997CF-0B37-45DC-8B87-A33FD4606F10}.png]]

## Risk- Attackers and Types of Attacks
![[{DA79D39A-EE2D-42F6-B462-C1A9DDB2C673}.png]]
![[{03B52D5A-AD79-4D93-B432-6D71E709E6E5}.png]]
![[{2A3B1F2A-8F7D-40AC-BCF5-B6B33A05D99A}.png]]
Outsider --> Paling sering melakukan serangan tapi paling sering gagal.
Insider --> Unlikely, but bahaya.

![[{8CAE2BB1-AE58-41DC-8768-4D3DB66A29BE}.png]]
![[{B6663829-91EA-40E2-9F2E-28FB98FC0E5D}.png]]

C2 --> Bot Herders --> Botnets (1000 bots)

![[{BC5F07C9-76AC-4001-B040-21A066AA3B6B}.png]]

## Business Continuity Planning (BCP) - Penting for Exam

![[{5972BB79-2DD9-4DB8-B246-A83AEC239EA7}.png]]
--> Disaster Recovery Plan (DRP)
--> Business Continuity Planning (BCP)

Penting. JANGAN anggap tidak akan terjadi. Harus sedia plan besar dan sub plan - sub plannya, agar ketika disaster, kita sudah tau harus apa prosedurnya.

What if? What if? What if? Identify semua gaps, scenario disaster, dan risknya.

--> Earth Quake or Flooding --> Two Data Centres, di beda region.

### BCP / DRP == NIST 800-34
![[{55D48070-6F18-4F7B-96AC-F7B14E5D6C35}.png]]
![[{7FD19C0C-97A1-4C44-AA99-6B3C9F6E770C}.png]]
Senior management needs to be involved and know the process.

### Business Impact Analysis (BIA), bagian dari BCP
![[{8D72C921-7FD6-49E5-9853-5ACA016F7EE6}.png]]
**RPO** (Recovery Point Objective) --> Acceptable amount of data that cannot be recovered
**MTD** (Maximum Tolerable Downtime) --> Seberapa lama downtime maximumnya.
**RTO** (Recovery Time Objective) -->Amount of time to restore the system 
**WRT** (Work Recovery Time) --> How much time is required to configure the recovered system

**MTD >= RTO + WRT**

That said, just in case, also know that MTD can be called 
- **Maximum Allowable Downtime - MAD** 
- **Maximum Tolerable Outage - MTO**
- **Maximum Acceptable Outage - MAO** or
- **Maximum Tolerable Period of Disruption.**

Just know all of these refer to the same thing.

Our MTD is made up by two variables, RTO and WRT.

![[{F23A07ED-B5C4-482D-A252-9EEACB114072}.png]]

**MTBF** (Mean Time Between Failures)
**MTTR** (Mean Time to Repair)
**MOR** (Minimum Operating Requirements) --> Spec terendah agar critical function bisa jalan dulu.

![[{173E7051-2781-4256-A482-522AB9DD49D0}.png]]

First, let's start out by defining what we mean by external dependencies.

**It is all the third-party services, suppliers, resources, that we need to maintain our normal operations.**

That can be cloud service providers, Internet service providers, raw materials, even key customers whose business is essential to our company's success.

![[Pasted image 20241026152007.png]]
![[Pasted image 20241026152101.png]]

Intinya ketika external dependencies ter-impact, kita harus sedia backup. Dan harus dinamis krn things are always changing.

C/o punya multiple external dependencies. Kyk CDC pake Jumio dan Onfido

![[{F5ED32AE-A4BA-4E49-87B2-A18D01EC4457}.png]]
![[{805081BD-FE57-4AE3-8DFB-7402F006B28A}.png]]

**Domain 1 Review**
![[Pasted image 20241026152903.png]]


# Domain 2
![[Pasted image 20241101125857.png]]

## Information Life Cycle
![[Pasted image 20241101130013.png]]

**Archiving vs Backup**
Archiving --> us keeping a copy for future use, just in case we might need it. A data archive, we keep for as long as the data is useful.
Backup -->  us taking a backup so we can restore the data. So a backup we keep to restore with. Over time they get less useful.

### Three States of Data
![[Pasted image 20241101130536.png]]
**Data at Rest**
	--> Backup tape, harus selalu being encrypted. Full disk ecryption.
	--> Avoid CD/DVDs, encryption di situ easy to break.
	**--> Bisa dienforce pake technical control**
**Data in Motion**
	--> Ecrypt the traffic. End2end ecryption.
	**--> Bisa dienforce pake technical control**
**Data in Use** (we are using the data, jadi gk bisa diencrypt)
	--> Clean desk policy. Clean cyber securiyy practices. No shoulder surfing, locking laptop, etc.
	**--> Mostly tidak bisa dienforce pake technical control. Harus training, awareness, dan administrative control kyk policy**
	--> Palingan technical control yg bisa diimplement adalah, auto lock screen laptop after 1 minute. OR printer yang cuma bisa dipake kalo kita swipe keycard kita.

### Data Classification Policies
![[Pasted image 20241101131251.png]]
![[Pasted image 20241101140402.png]]
![[Pasted image 20241101140438.png]]

### Data Handling, Data Storage, and Data Retention
![[Pasted image 20241101140627.png]]

--> Di ujian, anggap kita selalu punya loggin terhadap siapa yang mengakses data.

MTD --> Maximum Tolerable Downtime.

Yang boleh membawa tape buat backup itu harus license dan held liable kalo tapenya kenapa-kenapa ketika in transit.

#### Retention
![[Pasted image 20241101140951.png]]

### Data, system, mission ownership, custodians and users
![[Pasted image 20241101141253.png]]
![[Pasted image 20241101141452.png]]

### Memory and Data Remanence
![[Pasted image 20241101145231.png]]
**Data Remanence**: sisa data after removal.
![[Pasted image 20241101145445.png]]
![[Pasted image 20241101145639.png]]

### Data Destruction
![[Pasted image 20241101145826.png]]
**Overwriting** --> Ada cases dmn masih bisa direcover meski udah ditimpa null byes.
**Sanitization** --> Cuma bikin infeasable aja, tapi masih bisa direcover, tapi susah bgt dan gk worth.
Purge --> Bener-bener gk bisa direcover lagi.

Tapi shreding, lebih recommended.

![[Pasted image 20241101152519.png]]

## Data Security Controls and Frameworks
![[Pasted image 20241101152853.png]]

## Data Protection (DRM, CASB, DLP)
![[Pasted image 20241101155754.png]]
**DRM** (digital rights management) --> Copyright, license key, kalo sharescreen gelap, etc.

**CASB** (cloud access security broker) --> Netskope. Monitor user activity, browsing activity, warn admins about possible malicious / dangerous actions. Malware preventions, shadow IT activities, **enforce compliance and policy**. Intinya ini adalah Gatekeeper. **CASB juga bisa berperan sebagai DLP di cloud environment**.

Shadow IT --> Intinya adalah user bisa menggunakan IT Resources yang di mana kita sebagai IT department tidak tahu.

**DLP** (Data Loss Prevention) --> Prevent data exfiltration.
Loss --> Laptop dicuri. Kita lose access ke datanya. or datanta didestruct. itu Loss
Leak --> Kita ke hack, datanya didownload attacker, tapi kita masih ada copynya. itu Leak.

Network DLP --> 
- Untuk **data in motion** (DLP bisa bantu jika datanya classified as sensitive, akan notify admin or require admin permission dulu or **datanya gk dikasih untuk keluar dari network perusahaan kita**)

Endpoint DLP --> 
- Untuk **data in use** (DLP bisa bantu untuk realtime untuk block action bila action tersebut gk seharusnya dilakukan) dan 
- **data at rest** (DLP bisa bantu untuk encrypt data dan enforce proper access control to it.)


# Domain 3 - The biggest domain out of all
25% of all of the Curricullum
- Security Architecture and Design
- Cryptography
- Physical Security

![[{9AFBDFF8-C18F-4B44-8C78-5DA63654C6EE}.png]]

### Security Models Fundamental Concepts
- Tipe-tipe access control
![[{144CF14B-7E50-4B6A-B842-EC9F9E7F77A1}.png]]
**Mandatory Access Control** (MAC) --> Highly secure, usually what we would have in the **military or in highly secure organizations.** And it is not you have top secret clearance, you can see everything that is top secret. You will most likely have access to a subset of a subset. It might be nuclear submarine at top secret level, and then you still might have to go through formal access approval.

**Role-based Access Control** (RBAC) --> Setiap role punya accessnya sendiri. Paling sering dipakai di organisasi. Jangan lupa kalo employee pindah divisi, hapus role lama, kasih role baru.

**Attribute-based Access Control** (ABAC) --> Much better system, most likely organization bakal switching ke ABAC. Karena bener-bener conditional dan lebih granular. Lebih secure dari pada RBAC. **Access is granted based on subjects, objects and environmental conditions. And attributes can be assigned to both subjects, objects, and something in the environment.**

The new thing here is **attributes**. This could be **where are you accessing it from**?**When** are you accessing it? 

This could be threat levels. Let's say you are a project manager. Your role and your clearance might give you access to an object, **but you are not on the project team working on that specific project**. Well, then you get rejected.

If you then get assigned to the project or you just need to help more, then all of a sudden you can access it. 

Let's say you are the data owner, **you have full access to everything**, **but if you are trying to access that object from a place where you shouldn't be or at a time that you shouldn't be, well, then the access is also denied**. Those environmental conditions or attributes, gives us a much more granular access model that I think is going to pick up over the next 10 years, and is much, much more secure than Role Based Access Control.

**Rule-based Access Control** (RUBAC) --> Ini seperti Firewall. **Tergantung rule yang kita set**. If apa, then apa. Kalau ada traffic dateng menuju port 80, block/drop the traffic.  Kalau ada traffic datang dari IP yang udh kita allowlist, allow. Gitu-gitu aja ez.

#### **Bell-LaPadula** (MAC, Confidentiality)

- Bakal keluar di EXAM
![[{38B3D787-C8B2-4E38-B6AC-95AE6CCA407F}.png]]
**Bell-LaPadula** is **only focused on confidentiality** and it is mandatory access control.

It was developed by the US Department of Defense and it is a state machine model.

Afalin no read up, no write down, no read up or write down. Afalin nama-namanya, star security property, dll.

#### BIBA (MAC, Integrity)
![[Pasted image 20241112134431.png]]
BIBA is also mandatory access control, but the whole purpose of BIBA is data **integrity**.

BIBA was also developed by the US DOD and it is a state transition model.

BIBA also has three properties or axioms, but remember, the focus is integrity.

No read down, no write up, no read or write up.


#### LBAC, Lattice Based Acces Control (MAC, juga)
![[Pasted image 20241112134653.png]]
Complex


#### Graham-Denning Model
![[Pasted image 20241112134736.png]]


#### HRU (Harrison, Ruzzo, Ullman)
![[Pasted image 20241112134814.png]]
Subject == Object di sini.

It is based on an extension of the Graham-Denning model and it is an operating system level security model that focuses on the integrity of access rights to the system.


#### Clark Wilson - Integrity
![[Pasted image 20241112134922.png]]
--> **Focuses on integrity**
--> It separates the users from the back end data through what they call well-formed transactions and separation of duties.
--> It uses subjects and objects that you are already familiar with, but it also uses a program which acts as an intermediary between the subjects and the objects.

Example:
Think of buying something on Amazon. If I go by a book, I can't go in and change how many books they have available. They allow me to add it to my cart, to pay for it, and **then the intermediary program that Amazon has subtracts one from the inventory once I have purchased or at least when they ship it**. Ada sistem yg otomatis ditengah. No human error or interaction with the integrity.

The separation of duties that Clark-Wilson. uses is the same one we have talked about already. We don't let Bob both issue a purchase order and then approve it. The same here, we do not let the same subject certify a transaction and then allow them to implement it.


#### Brewer-Nash (Chinese Wall model)
![[Pasted image 20241113110920.png]]
--> Gambar di kanan itu buat Non-Interference Model.

#### Take-Grant Protection Model
![[Pasted image 20241113111017.png]]

#### Access Control Matrix
![[Pasted image 20241113111041.png]]

#### Zachman Framework (5W + 1H)
![[Pasted image 20241113111141.png]]

#### Security Models
![[Pasted image 20241113111214.png]]
![[Pasted image 20241113111251.png]]
![[Pasted image 20241113111317.png]]

## Evaluation Methods, Certification, and Accreditation
![[Pasted image 20241113111532.png]]
We need to know the **Orange Book** (computer system) and the **Red Book** (network).

![[Pasted image 20241113111647.png]]
![[Pasted image 20241113111742.png]]
**EAL Level 1-7 ini HARUS DIAFAL BUAT EXAM.**

### Secure Design Principles
![[Pasted image 20241113111858.png]]
![[Pasted image 20241113134354.png]]
![[Pasted image 20241113134513.png]]
Threat Modeling
PASTA (Attacker Focused) - Process for Attack Simulation and Threat Analysis

![[Pasted image 20241113134640.png]]
STRIDE (Developer Focused) --> Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege

Trike (Acceptable Risk Focused)

Dread  --> Abandonden by Microsoft in 2008. 
--> Disaster/Damage, Reprorducibility, Exploitability, Affected Users, and Discoverability (DREAD)

![[Pasted image 20241113134928.png]]
Kalo asal Trust bahaya, admin account compromised, the end.

**Zero Trust** -> **NIST SP 800-207**. We don't trust anyone. Even udah pass certain perimeter and verification, tetap harus authenticate. 

That is, we don't trust any device on our network, even if that one device has been verified. Every time a subject needs to access a device or an application, we both authenticate and authorize both of them.


### Secure System Design Concepts
![[Pasted image 20241113142911.png]]
Layering != OSI model, beda hal.

A layer can only interact with the layer next to them.

![[Pasted image 20241113143047.png]]
![[Pasted image 20241123100413.png]]

As I mentioned, this is a conceptual model. It is idealized. And in actuality, we really only use ring 0 and ring 3. 1 and 2 have been collapsed because we want to make the applications faster.

**That said, still no ring 0, 1, 2, and 3 for your exam**. And then finally and noteworthy mention, we also have something we call **ring -1** and that is **hypervisor** mode and that is used if our system is a **virtual machin**e.

Then below ring 0, there would be the hypervisor, if it is not a virtual machine, well then we would stop at ring 0.


## Managing Information System Lifecycle

![[Pasted image 20241124204138.png]]
![[Pasted image 20241124204225.png]]
**Operation and maintenance**: The longest phase of the cycle

![[Pasted image 20241124204444.png]]
![[Pasted image 20241124205931.png]]

## Secure Access Service Edge (SASE)
![[Pasted image 20241124210023.png]]

Penting, lebih kepake sekarang karena most organization udh 100% cloud sekarang. Not even physical infrastructure yang bisa dikontrol

![[Pasted image 20241124210105.png]]
![[Pasted image 20241124210428.png]]
![[Pasted image 20241124210604.png]]


## Hardware Architecture

**Legacy Computer Architecture**
![[Pasted image 20241124210724.png]]

**Now Architecture** (Separate antara nothbridge and southbridge)
![[Pasted image 20241124210812.png]]

The closer you are the CPU the faster it gets. Makannya Northbridge is faster.

![[Pasted image 20241126122029.png]]

CPU Functionality
![[Pasted image 20241126122320.png]]
![[Pasted image 20241126122354.png]]
![[Pasted image 20241126122642.png]]
![[Pasted image 20241126122710.png]]
![[Pasted image 20241126122831.png]]
![[Pasted image 20241126122930.png]]

The BIOS is stored in Read-Only Memory. On systems now, that means EEPROM. You may see an EPROM every so often, but you should never ever see a real just ROM or PROM. Because they are so old, so legacy, we should not have them in our environments. Them only being able to be programmed once is a security issue. The BIOS being stored in EEPROM can also be a security issue. **Remember, electronically erasable. That means that the skilled hacker can go in and change the lower-level operating system if we do not have enough other security controls in place**.

![[Pasted image 20241126123542.png]]

**Microservices**
![[Pasted image 20241126123757.png]]
Microservices > Monolith.

![[Pasted image 20241126123916.png]]
![[Pasted image 20241126124016.png]]
Serverless == FaaS (Function as a Service), Lambda.

#### Secure OS and Software Architecture
![[Pasted image 20241126124146.png]]
![[Pasted image 20241126124302.png]]

## Virtualization, Cloud, and Distributed Computing (IMPORTANT FOR EXAM)

#### Virtualization

![[Pasted image 20241126124631.png]]
![[Pasted image 20241201210443.png]]
![[Pasted image 20241201210624.png]]

Type 1 == Data centre, enterprise
Type 2 == Home usage

For the exam, I would know the difference between a type one and Type two hypervisor, their strengths and weaknesses of both and where we would use them. **For our data centers, it would make no sense to use Type two hypervisor because that extra layer is just going to eat up a lot of resources. In home environments, Type one doesn't really make sense either**. We pick the right implementation for what we are doing.

**VM Risks**
![[Pasted image 20241201210846.png]]

We want to keep an eye on resource utilization on our VM hosts so we know when we're getting close and we know the resource utilization trends so we can predict in six months we are out of resources.

#### Cloud Computing
![[Pasted image 20241201211129.png]]

**Private Cloud** --> Kita bikin cloud kita sendiri
**Public Cloud** --> AWS, GCP, Azure
**Hybrid Cloud** --> Mix of private and public.
**Community cloud** --> Only for use by a specific community of consumer from organizations that have shared concerns (mission, policy, security requirements).

**Cloud Shared Responsibilities**
![[Pasted image 20241201224850.png]]

**IaaS** --> Client responsibilities == ASDO (Apps, Security, Database, OS, ada firewall juga kadang)
**PaaS** --> Client responsibilities == A (Apps)
**SaaS** --> Client responsibilities == Data doang harusnya

**Grid Computing**
![[Pasted image 20241201225243.png]]
![[Pasted image 20241201225310.png]]
Much of copyright infringement happens on peer to peer networks.

![[Pasted image 20241201225447.png]]

Thin Client Application kyk VDI gitu gk sih.

**Distributed Computing**
![[Pasted image 20241201225617.png]]
**Distributed Computing** **Environment** (DCE) == The user connect to whatever the closest. (One of the example is blockchain)

**CDN (Content Delivery Network) is a DCE but not all DCEs is a CDNs.**

Blockchain == Super high integrity. Satu block keubah, harus rehash semua block.

![[Pasted image 20241201230009.png]]

Edge Computing == Salah satunya adalah CDN (contoh paling simplenya.)

### IOT (Internet of Things)
![[Pasted image 20241201230234.png]]
Gk secure, karena biasanya dedesign buat functionality instead of security. **Most of them uses well-known ports and default passwords.** Lebih bahaya lagi apalagi semuanya connect ke internet.

Biasanya IoT devices juga tidak well maintained patchesnya. Gk ada proper patch management. Karena susah buat patch devicenya kalo udah dideploy (inability to patch / update the software).

## Emanations and covert channels

Emanation == Emanasi == an abstract but [perceptible](https://www.google.com/search?sca_esv=d608386cb98ae779&sxsrf=ADLYWIIhA6aSvqrglmd486U6wpncjTTwBQ:1733678227753&q=perceptible&si=ACC90nwZrNcJVJVL0KSmGGq5Ka2YLKsPTpWhaTFDKj6YTBOp018N0z1FogLaLt0xS5UPEpW0GQ08jRzwl9dbPnsv3hBS9sYnsTkf52OG6hvQeThCs8z-1jM%3D&expnd=1&sa=X&ved=2ahUKEwix5K3X1piKAxWGRmwGHWTIJ24QyecJegQIQBAO) thing that issues or [originates](https://www.google.com/search?sca_esv=d608386cb98ae779&sxsrf=ADLYWIIhA6aSvqrglmd486U6wpncjTTwBQ:1733678227753&q=originates&si=ACC90nz-2feRzoY4yuySkO-aQE811hW-D8YePk2xNKKVVMiAj_Q0V5qMUnS9JvrRgYjcORgQNylJwOnqYhR17HDg-QqZGrOS_JTOGHkPk4Q9hhXDTSkIaII%3D&expnd=1&sa=X&ved=2ahUKEwix5K3X1piKAxWGRmwGHWTIJ24QyecJegQIQBAP) from a source.

Kyk side channel attack (?)

![[Pasted image 20241209001803.png]]

If you are sending a text message and the attacker has access to your motion sensor on your phone, then your phone will move slightly left, right, up, down. Whenever you text, the motion sensor can detect that. And that is enough to reassemble your messages just from that movement.

**Any emanation is really just an unintentional information bearing signal that if intercepted and analyzed, can lead to compromise and** **we can technically protect against emanations by using heavy metals and encasing whatever we have barring the signal**.


Covert Channels, **intentionally creating the capability to transfer information using channels it was not intended for**.
--> Most common buat user enum. analyze the difference between response.

Another way an attacker could use a covert storage channel could be if we do not have ICMP packets blocked outwards, they can either have the payload in the outbound ICMP package or they can just send the package to a certain IP at a certain port. And the combination of the IP and the port could respond to a letter or a word, and then the information could be assembled by whomever that is sent to.

![[Pasted image 20241209002242.png]]
**Steganography** --> Hiding secret inside a media (image, audio, etc.)

**Digital Watermarks** --> Let's say I go on Amazon and I buy a study guide for the exam. I download it as a PDF, then either visibly or invisibly, it has a watermark identifying it as mine. Now, if I decide to share that with other people, then my personally identifiable information is embedded in that file. If they find it on a website sharing illegally downloaded materials, it will say this file was purchased by Thor Pederson. Ketangkep deh siapa yang ngebocorin.

## Malware
**Common types of Malware**
![[Pasted image 20241210142216.png]]

you are not going to see definition questions on the exam. That means you're not going to see what is a stealth virus.

What you are going to see is application or how we would protect against a certain type of malware or in this scenario, what would you do?

So you need to learn what each type is, how it compromises our systems and what we can do to protect against it. You may see a paragraph of text and somewhere in there there is alter signature or embedded. And from those keywords, you know which type of malware it is, then you also know what can we do to protect against it and what can we do once we are infected?


**Viruses** are one of the most common types of malware. **They require some sort of human interaction** and they most commonly infect our systems from USB drives or any other portable device.
--> **Macro Virus** = Pake macro di documents
--> **Boot Sector** = Boot sector virus, it's in the boot sector, which is a great place to hide a virus, because remember, the boot sector is the underlying OS that boots before the real OS. Which is also why many antivirus and malware programs can be set to run on the boot sector before this system loads it completely.
--> **Stealth Virus** = **Tries to hide themselves**
--> **Polymorphic** = Change their signature to avoid AV signature definitions
--> **Multipart** = Ada multiple part. Spread across multiple vectors. That means that part of it could be in the OS and part of it could be in the boot sector. Susah dibersihin.

![[Pasted image 20241210142841.png]]
**Worm** = Spread on it's own, no need for human interaction. Easy to detect.
**Trojan** = Malicious code embedded in a program that's normal.
**Rootkits** = Replace some part of OS/Kernel with malicious payload. 
	If it is a user rootkit, then it will be on Ring 3,
	if it is a kernel rootkit, then it is Ring 0.

And remember, the kernel is the thing that loads before the OS. So unless our boot sectors are scanned before they load up, this could be a real problem because it loads first every time.

**Logic Bombs** = Logic bombs are based on a certain time or a certain event. **Unless the logic in that malware is fulfilled, it does nothing**. It stays dormant and it is simplistically just based on IF-THEN, if this happens, then do that.

That could be, if Bob doesn't get a ten thousand dollar bonus this year, then the malicious code executes. **Or if the date is 5/15 2022 at 2:12, then execute the malicious code**.

![[Pasted image 20241210143216.png]]
**Packers** (Software legit yang suka dipake malware) = are programs that are used to compress executable files. They're not good. They're not bad. **They are neutral technology**. They are, however, important to malware because the bad actors will also use them. This could be the program that you downloaded illegally that does really contain the right program. But it also has the Trojan we talked about before, and it doesn't necessarily have to be on bad sites. It could be the real site. If the hacker has been able to hack the website and upload their compromised file with their Trojan, then how would you ever know? **And the answer here is you look at the hash**, remember, hashes are a one way function, the same plaintext, all the same file should give you the same hash if nothing was altered. But if they have added a Trojan to the program, then the hash is going to be different. So neutral technology that can be used for bad things.

**Antivirus** = They used to be either signature based or behavioral based. Now they're both. Heuristic (behavioral based, bisa jadi sering false-positive, but we need this krn malware zaman skrng udah gampang hide dari signature based detection)

![[Pasted image 20241210143604.png]]
**Server (service) Side Attacks** (hacker nyerang kita.) = a service side attack is someone attacking a target. They come most often from outside our organization and they attack a target. **They are very specific on going to that one target**. Kalau kita kurang defense in depth, dll, pasti jebol.

**Client-Side Attacks** (user melakukan hal tolol) = The client-side attack is something we as the user initiate. We go to them and get infected with some malicious content in a Web browser, instant messaging or something like that. Kalo kita melakukan hal tolol pasti jebol.

**Server, service side attacks can be much harder to accomplish if the target has a great defense in depth**, which hopefully we do.

**Client-side attacks are often more successful because we go out and do something that we shouldn't**, we established the session and that might bypass some of our security measures.

**Server side attacks are successful when we don't do something that we're supposed to, client-side attacks are successful when we do something we shouldn't have.**

## Web Architecture and Attacks
![[Pasted image 20241210144256.png]]

Security should always be a part of the design process, just like the functional requirements.

**OWASP (Updated every 4 years)**
![[Pasted image 20241212234110.png]]

**XML (Extensible Markup Language) and SOA** **(Service-Oriented Architecture)** 
![[Pasted image 20241212234154.png]]

XML is a standard way of encoding documents and data. It is somewhat similar to HTML- Hypertext Markup Language, but it is more universal, whereas HTML is only used for the web. XML is mainly used for the web, but it can also be used outside of the web. It can, for instance, be used to store application configuration outputs from auditing tools and many other things.


SOA or Service Oriented Architecture is a style of software design where services are provided to all the components. Very simplified, it is your code broken into reusable modules, and it has been used for many years. The only difference now is we can do it over a network. It can act as a bridge between the back end data and our applications. You can also think of it like the separation we have between the hardware, the kernel, the drivers and the operating system.

The operating system doesn't really care which kind of hardware it runs on. It has that layer in between the kernel and the drivers. This is somewhat similar. The application and the backend data don't really care about each other. They just need some sort of medium they can communicate through, which is the service oriented architecture.

## Database Security
![[Pasted image 20241212234925.png]]
**Poly-instantiation (Multiple instatiation or multiple instance)**
--> 1 File yang sama tapi isinya bisa beda tergantung yang buka. Bisa jadi dibedain by secret clerance usernya. Kalo yang buka adalah user Top Secret, maka isinya akan jadi confidential. dan sebaliknya.

Data analytics (an on-going process) != Data mining.

## Mobile Device Security (Phone, USB, CD, Laptop, etc. intinya anything mobile yg bisa dibawa)

![[Pasted image 20241218121230.png]]
- Remote wipe
- Full disk encryption
- Lock screen
- Device Tracking
- Account Lockout
- Disable removable storage
- MDM (Automatic update dan push configuration scripts secara global ke semua device. Guna bila device kita kalo udah banyak, kyk Airwatch)

![[Pasted image 20241218121838.png]]
![[Pasted image 20241218122034.png]]

## ICS (Industrial Control Systems)
![[Pasted image 20241218122311.png]]
ICS is an umbrella term we use for the control system and associated instrumentation used in industrial production technology. OT (?) kah

What that really means is it is a way for us to monitor and automate production plants. And no, those are not potted plants.


SCADA --> Command and Control untuk sistem pabrik. 

The PLC is for smaller setups and is something we would use if our IO points were not more than a couple of thousands.

![[Pasted image 20241218122555.png]]

## Cryptography
![[Pasted image 20241218122836.png]]

As with anything else we do, we want exactly enough encryption. Not too much. Not too little. We want our encryption to be so strong that it is unbreakable or at least it's going to take an unreasonable amount of time to break it.
![[Pasted image 20241219153152.png]]
![[Pasted image 20241219153355.png]]
![[Pasted image 20241219153531.png]]
![[Pasted image 20241223132759.png]]
![[Pasted image 20241223132921.png]]
![[Pasted image 20241223133038.png]]
![[Pasted image 20241223133115.png]]
![[Pasted image 20241224180529.png]]
![[Pasted image 20241224180923.png]]
![[Pasted image 20241229211552.png]]
![[Pasted image 20241229211621.png]]
![[Pasted image 20241229211927.png]]


## Symmetric Encryption
### DES (AFALIN MODE-MODENYA)
![[Pasted image 20241229212140.png]]
![[Pasted image 20241229212310.png]]
![[Pasted image 20241229212352.png]]

### AES, Blowfish, Twofish (AFALIN MODE-MODENYA)
![[Pasted image 20241229212605.png]]
![[Pasted image 20241229212651.png]]
![[Pasted image 20241229212723.png]]
![[Pasted image 20241229212739.png]]

**Feistel**
![[Pasted image 20241229212815.png]]

### RC4, RC5, RC6
![[Pasted image 20241229213019.png]]


## Asymmetric Encryption
![[Pasted image 20241229213232.png]]
![[Pasted image 20250101095010.png]]
![[Pasted image 20250101095123.png]]
![[Pasted image 20250101095236.png]]

**ECC (Eliptic Curve) --> Patented, jadi berbayar**

![[Pasted image 20250101095335.png]]

## Hashing
![[Pasted image 20250101095537.png]]
- It only protect Integrity but **doesn't provide confidentiality**.

![[Pasted image 20250101095816.png]]
![[Pasted image 20250101095908.png]]
![[Pasted image 20250101100024.png]]
![[Pasted image 20250101100056.png]]

Nonce sama aja kyk salting. Baca aja.

## Quantum Computing and Quanting Cryptography

![[Pasted image 20250101100417.png]]
![[Pasted image 20250101100433.png]]
![[Pasted image 20250101100643.png]]
![[Pasted image 20250101100722.png]]
![[Pasted image 20250101100742.png]]

## Attacks on Cryptography
![[Pasted image 20250101100909.png]]
![[Pasted image 20250103131528.png]]
![[Pasted image 20250103134422.png]]
![[Pasted image 20250103134715.png]]
![[Pasted image 20250103134816.png]]
![[Pasted image 20250103134936.png]]
![[Pasted image 20250103135057.png]]
![[Pasted image 20250103135205.png]]
![[Pasted image 20250103135242.png]]
![[Pasted image 20250103135313.png]]

### Digital Signatures
![[Pasted image 20250103135416.png]]
![[Pasted image 20250103135600.png]]
![[Pasted image 20250103135831.png]]
![[Pasted image 20250103135908.png]]
OCSP --> Yang sekarang dipake. It's faster.

### MAC, HMAC, SSL, TLS
![[Pasted image 20250103140213.png]]
![[Pasted image 20250103140320.png]]

### IPSEC (IMPORTANT) and PGP
![[Pasted image 20250103140449.png]]

With IPv6, IPSEC is built in.

Kalo di IPv4 itu Addon aja.

![[Pasted image 20250103140630.png]]
When we use IPSEC, we can either use it in **tunnel mode or in transport mode**.

**In tunnel mode (THE MOST COMMON USED MODE IN IPSEC), we encrypt and authenticate the entire data package, including the headers, and we use tunnel mode for systems that does not natively speak IPSEC.**

**In transport mode. Here, we only encrypt and authenticate the payload. Everything else is left as is because the two systems know how to talk to each other already.**

![[Pasted image 20250103140713.png]]

IKE --> this helps the system to **choose the fastest and most secure type of encryption and hashes that both sides can use.**

**PGP**
![[Pasted image 20250103141039.png]]

# Physical Security
![[Pasted image 20250103141342.png]]

Bollards --> Sesuatu penjaga yang mencegah mobil / kendaraan buat lewat. Kyk tiang besi / beton, etc.

**Deterrent Controls** --> Yang bikin takut / discourage dan membuat orang mengurungkan niat untuk menyerang.

**Compensating Controls** --> controls that **we implement to compensate** for other controls that either are impossible or simply too expensive. Contohnya, daerah Data centre kita rawan banjir. Dan kita gk bisa pindahin, jadi untuk mengcompensate itu, kita bikin sesuatu buat mencegah banjir, seperti penyerap air di servernya, etc.

**Administrative Controls** --> Policies, procedures.

![[Pasted image 20250105131821.png]]
![[Pasted image 20250105131911.png]]
![[Pasted image 20250105132127.png]]

And they are hooked up to a DVR, a digital video recorder, which then stores the recordings on either a local server or device or on a network video recorder, NVR.

In good security design, we would want the NVR or the remote network location over a local storage.

![[Pasted image 20250105132528.png]]
![[Pasted image 20250105132614.png]]
![[Pasted image 20250105132701.png]]
![[Pasted image 20250105132810.png]]
![[Pasted image 20250105132916.png]]
Data kita itu distore di dalam ICCnya. 

![[Pasted image 20250105133122.png]]
![[Pasted image 20250105133326.png]]
![[Pasted image 20250105133418.png]]
![[Pasted image 20250105133506.png]]
![[Pasted image 20250105133724.png]]
![[Pasted image 20250105134116.png]]
![[Pasted image 20250105134200.png]]
![[Pasted image 20250105134250.png]]

### Physical Security - Site Selection (Cara pilih lokasi datacenter / site yang baik)
![[Pasted image 20250105134550.png]]

Greenfield --> Undeveloped land. Untouched land.
Topography --> Bentuk tanahnya.
Utilities --> How reliable is the power, the internet in the area.


![[Pasted image 20250105152448.png]]
![[Pasted image 20250105152558.png]]
![[Pasted image 20250105152647.png]]
![[Pasted image 20250105152810.png]]
![[Pasted image 20250105153210.png]]

### Media Storage and Locations
![[Pasted image 20250105153515.png]]

### Asset Tracking and Hardware Hardening
![[Pasted image 20250105153822.png]]

### Electricity
![[Pasted image 20250105154316.png]]

**UPS** - uninterruptible power supplies. Remember, those are the big banks of batteries and you can see a picture over here on the right, well, you see those rows and rows of batteries.
**PDU** - power distribution unit. **the PDUs ensure that we have** **the clean power, that the voltage is not too high or too low/ just right voltage jadi gk over dan bikin korslet.**

![[Pasted image 20250105154623.png]]
![[Pasted image 20250105154823.png]]

And that is called crosstalk. Since electricity from one cable can affect another, this can damage our integrity. The data is going to be corrupted. And not only our copper Ethernet cables susceptible to crosstalk, they can also be a problem for our confidentiality. Someone can clamp a sniffer on the cable and they can then pick up our traffic, which is why it is so important that all our traffic is encrypted.


**From an IT security standpoint, fiber cables are always preferable over copper. They're not susceptible to EMI.**

**They can't be sniffed very easily, which then makes them much more secure.**

Cheapest-secure == Fiber optics, bukan Copper. Yes copper lebih murah tapi gk secure.


**Power Fluctuations** --> Will affect Availability. Power fluctuations could cause system downtime or hardware damage, thus seriously impacting the availability of the system. While severe power issues could potentially lead to loss of data (impacting integrity) or temporary exposure of data (impacting confidentiality), these impacts are less direct and less likely than the impact on availability."

### Environmental Controls
![[Pasted image 20250105155302.png]]

Too cold is expensive and not good.

![[Pasted image 20250105155555.png]]
![[Pasted image 20250105155809.png]]

![[Pasted image 20250105155839.png]]

### Fire Supression
![[Pasted image 20250105160022.png]]

**FM200 Fire Supression**
![[Pasted image 20250105160103.png]]
![[Pasted image 20250105160153.png]]
![[Pasted image 20250105160222.png]]

In our data centers and most of our office locations, we would probably use orange, red and maybe yellow bulbs, nothing higher.

![[Pasted image 20250105160356.png]]
![[Pasted image 20250105160545.png]]
![[Pasted image 20250105160651.png]]
![[Pasted image 20250105160801.png]]

Fire Extinguisher ada class-classnya. Cuma boleh dipake di api yang sesuai classnya.

![[Pasted image 20250105160930.png]]

Remember, A for ash, when it burns, it turns into ash.

Type B is flammable liquids and gas. Think B for a barrel, liquids are in a barrel.

Type C is electrical equipment. Think C for current like the power we use for our servers, that is current.

Type D is combustible metals, think D- dynamite. It explodes, it is combustible.

Type K that is oils and fats that are burning. Think K for kitchen.

**Sprinkler System** --> Most effective fire prevention security controls for detection and suppression.

**Photoelectric Detector** --> Photo itu cahaya, berarti fokus ke **Smoke**, karena smoke obscures light.

Which of the following is the MOST important indicator of a well-functioning HVAC (Heating, Ventilation, and Air Conditioning) system? **Proper Airflow**

Kenapa? Proper airflow is critical for maintaining a stable environment, especially in heat-generating areas like data centers. Adequate airflow ensures efficient **distribution of cool air** and effective **removal of hot air**, maintaining consistent temperature and preventing overheating.

### Personnel Safety
![[Pasted image 20250105161558.png]]
![[Pasted image 20250105161757.png]]
![[Pasted image 20250105162026.png]]
INGAT, HUMAN IS THE MOST IMPORTANT.

![[Pasted image 20250105162111.png]]


# Domain 4 - Communication and Network Security

![[Pasted image 20250105163730.png]]

### Networking Basics and Definitions
![[Pasted image 20250105163820.png]]

Afalin nih simplex, duplex, etc.

**Simplex** --> Radio, 1 arah.

Half-duplex itu kyk Walkie talkie --> Ngomongnya gk bisa bareng, harus ganti-gantian. One at a time.

**Full-Duplex** --> Telephone, voice call.

**Baseband** --> Ethernet. 1000base-T == STP cable is a 100 megabit baseband Shielded Twisted Pair cable.

Internet 

Intranet --> Organization internal network

Extranet --> Connection between private intranets. Seperti kita bisa connect ke network bisnis lain.

![[Pasted image 20250106100629.png]]
![[Pasted image 20250106102732.png]]

## OSI Model (Important-important for exam)
![[Pasted image 20250106103056.png]]

Afalin PDUnya.

Layer 1 --> Bits
Layer 2 --> Frames
Layer 3 --> Packets
Layer 4 --> Segments
Layer 5 - 7 --> Data

![[Pasted image 20250106114206.png]]

Layer 1
![[Pasted image 20250106103337.png]]

Expensive -> Fiber
Cheap -> Copper
Cheap-Secure -> Fiber
Secure -> Fiber

Layer 2
![[Pasted image 20250106112241.png]]
Layer-2 --> MAC Address.

MAC Address must be unique in that local network.

With IPV4, we can use both 48 and 64bit devices, whereas IPV6 can only use 64bit Mac addresses.

If we use IPV6 and we have devices on our network that are only 48bit Mac addresses, then IPv6 will just seam in another 16 bits into the Mac address, effectively making the 48 bit a 64 bit Mac address.

**The most common threats on layer two are Mac spoofing and Mac flooding.**

Carrier Sense Multiple Access (CSMA) 
-> Collision Detection (CD)
-> Collision Avoidance (CA) 

Mencegah network collision.

Collision paling sering di HUB. Switch udh lebih aman.

Layer 3
![[Pasted image 20250106112725.png]]
TRICK: **SEMUA PROTOCOL YANG MULAI DENGAN HURUF I ADALAH LAYER 3 PROTOCOL, KECUALI IMAP (LAYER** 7)

Layer 4
![[Pasted image 20250106112816.png]]
SSL/TLS --> Masuk ke layer 4 - layer 7

![[Pasted image 20250106113014.png]]

The bigger the layer the slower and smarter it gets.
Layer 1 --> It's just 1 and 0, its fast.

Semakin nambah layernya, semakin banyak data yang ditambahkan.

Layer 7 --> Datanya udah banyak di sini, semakin slow.


Layer 5, 6, 7 (Data, saling integrated mereka)
![[Pasted image 20250106113625.png]]

**TRAFFIC IS BEING ENCRYPTED ON LAYER 6.** 
--> SSL/TLS

Active Directory Integration --> Layer 7

![[Pasted image 20250106113727.png]]

HTTPSnya itu di layer 7. TETAPI PORT NUMBER itu di Layer 5. JGN SALAH

Jadi kalau ditanya port 443 di layer mana, itu di layer 5 (session layer)

Kalo HTTPS di layer 7.


### TCP / IP Model or Internet Protocol Suite or DOD Model
![[Pasted image 20250106113924.png]]

-> Cuma ada 4 layer instead of 7.

1. Link and Physical Layer / Network Access Layer
2. Network Layer
3. Transport Layer
4. Application Layer

![[Pasted image 20250106114141.png]]

Link and Physical Layer
![[Pasted image 20250106114312.png]]

Network Layer
![[Pasted image 20250106114321.png]]

Transport Layer (TCP, UDP, dan port number)
![[Pasted image 20250106114421.png]]

Application Layer
![[Pasted image 20250106114505.png]]

**How packet travel**
![[Pasted image 20250106114657.png]]

Dari kita buka website (dari application), sampe ke targetnya (ke applicaiton lagi). Fascinating.

### IP Address, Mac Address, and Port
![[Pasted image 20250106114923.png]]

Kalo device 48Bit, IPV6, akan nambahin FF:FE di tengah biar jadi 64bit.

![[Pasted image 20250106133518.png]]
![[Pasted image 20250106133723.png]]
![[Pasted image 20250106133818.png]]

![[Pasted image 20250106134217.png]]
![[Pasted image 20250106134304.png]]

Traffic Types
![[Pasted image 20250106144740.png]]
Unicast - 1 to 1
Multicast - 1 to many
Broadcast - 1 to all (yang di sent ke situ, di sent ke semua)

### IPv4
32bit
![[Pasted image 20250106144909.png]]

![[Pasted image 20250106145141.png]]

![[Pasted image 20250106145518.png]]
Yang kita pake di rumah itu PAT. Jadi, gmn caranya 1 Public IP bisa dipake bnyk private IP (devices). Ternyata dia differenciate by port.

![[Pasted image 20250106145643.png]]
![[Pasted image 20250106145818.png]]

### IPv6
128bit
![[Pasted image 20250106145921.png]]

IPSec is built in to IPv6, whereas with IPv4, it is just bolted on. IPv6 is still happening behind the scenes, you as a consumer rarely see it. I think three out of the four last Internet connections I had were IPv4, the newest one, the fiber connection is IPv6, where we're seeing really heavy use is IoT devices, cell phones, and then the service providers themselves, the long haul providers and all of the other stuff that we don't see as customers.

![[Pasted image 20250106150227.png]]
![[Pasted image 20250106150713.png]]

### Protocols

### ARP
![[Pasted image 20250106150809.png]]
--> Nyari IP relate ke MAC Address mana (device mana)
--> Ada RARP (Reverse ARP) --> Resolve MAC address to IP.

### ICMP
![[Pasted image 20250106150906.png]]
Ping, Traceroute, mastiin resource is up.

Ada TTL. 
128 ms --> Windows
64 ms --> Linux.s

### Traceroute
![[Pasted image 20250106151054.png]]
Tiap router, ngurangin TTL 1. Terus kirim ulang dengan TTL lebih besar. Cari Brp Hop untuk capai target kita dan lewat mana saja.

Max 30 Hops.

### SSH and Telnet
![[Pasted image 20250106151213.png]]

SSH Should not be considered secure, karena CIA bisa decrypt SSH.

![[Pasted image 20250109235956.png]]

Regular FTP is like Telnet for SSH. Regular FTP is not secure, even for internal. Use **SFTP** or **FTPS**.

### Email Protocols
![[Pasted image 20250110000118.png]]

### DNS
![[Pasted image 20250110110001.png]]

### SNMP (Simple Network Management Protocol)
--> Buat monitor devices di dalam network.
![[Pasted image 20250110110138.png]]

it can either report up or down or in version two or three, we get a lot more granularity. In version two and three, we can see a device traffic utilization, the internal temperature, memory use, how much of the hard disk is used, what percentage the HVAC is running at, how much battery power is left on our UPS and on and on.

So a very useful tool to keep an eye on our environment and it can help us prevent future incidents.

SNMPv1 and SNMPv2 itu cleartext. Bahaya.

SNMPv3 skrng udh encrypted.

Cuma orang malas upgrade ke SNMPv3.

### HTTP and HTTPS
![[Pasted image 20250110110424.png]]
HTML is what we send. HTTP is how we send it.

### BOOTP and DHCP
![[Pasted image 20250110110552.png]]

Biasanya static IP diassign ke device yg matters aja kyk Server. Biasanya workstation dynamic.

## Cables
![[Pasted image 20250110110926.png]]
![[Pasted image 20250110133608.png]]
UTP cable yg paling sering dipakai.

STP Lebih secure dari EMI tapi mahal.

Connector yg paling sering dipakai itu RJ45 buat modem, switch, router.

Buat telepon biasanya RJ11.

Ada juga cable Coaxial buat modem ke ISP, ato gk TV.

![[Pasted image 20250110133808.png]]

**Fiber Optic** --> Kabelnya bisa panjang bgt karena tidak ada atenuation. Lebih secure juga. Tapi mahal dan lebih susah digunakan. Dalemnya kaca, jadi gk bisa dibend bgt. Sekali patah, rusak kabelnya.
![[Pasted image 20250110134801.png]]

![[Pasted image 20250110134913.png]]
Satuannya, KIlobit, megabit, gigabit, terabit, petabit per second.

Data center biasanya pake Fiber karena di speed is so good.

### LAN Topologies, Technologies, and Protocol
![[Pasted image 20250110135115.png]]

Copper Ethernet berbeda dengan Fiber Ethernet.

![[Pasted image 20250110143052.png]]
![[Pasted image 20250110143202.png]]

Kabel pake ethernet kita bisa liat siapa aja di jaringan. Kalo WIFI, kita cuma bisa liat access point aja. Makannya harus RTS (request to send) dan kalo dikasih CTS (Clear to send) sama router baru kita bisa kirim packet.

![[Pasted image 20250110143319.png]]
![[Pasted image 20250110143330.png]]
![[Pasted image 20250110143425.png]]

Semua topology Legacy kecuali Star dan Mesh, karena kita masih pake itu sekarang. Mencegah single point of failure.

![[Pasted image 20250110143458.png]]


## WAN (Wide Area Network) Technologies and Protocol
![[Pasted image 20250110143646.png]]
![[Pasted image 20250110143753.png]]
SVC gk selalu up.

![[Pasted image 20250110143904.png]]

#### Yang sekarang dipake

**MPLS**
![[Pasted image 20250110143954.png]]

**SD-WAN (Software-Defined Area Network)**
- PENTING NIH, DIPAKE SKRNG
![[Pasted image 20250110144048.png]]

**SDLC, HDLC**
![[Pasted image 20250110172140.png]]

**DNP3**
![[Pasted image 20250110172218.png]]

**SAN (Storage Area Network) and VoIP Protocols**
![[Pasted image 20250110172309.png]]

VSAN mirip VLAN, kita segment network.

![[Pasted image 20250110172413.png]]

![[Pasted image 20250110172456.png]]
VoIP itu pake UDP. Sama kyk nonton video, lose packet dikit-dikit no worries.

VoIP bisa dipake buat text messages, video, phone calls. jadi gk cuma phone calls.

Cheaper and easier to implement, but then segala yang connect ke internet itu gk secure.

![[Pasted image 20250110172736.png]]
Backup if internet mati. Makannya harus sedia Analog Phone.

VoIP Protocols ada SIP (Session Initiation Protocol), H.323, MGCP, RTP, RTCP, etc.

SD-WAN itu bagian dari SDN.

![[Pasted image 20250110172922.png]]

![[Pasted image 20250110173053.png]]
Star most commond for enterprise, bukan Mesh. Karena Mesh kemahalan to implement. Butuh banyak network card and cables.

![[Pasted image 20250110173138.png]]
Disadvantage utama dari fiber optic adalah harganya. Setelahnya baru Gampang rusak, susah to install and gk flexible.

## WLAN (Wireless LAN) - WiFi
![[Pasted image 20250110173226.png]]

Most of the modern WLAN are based on IEEE 802.11

![[Pasted image 20250112170137.png]]
![[Pasted image 20250112170614.png]]

2.4ghz lebih banyak dipake.
5ghz band lebih jarang.

![[Pasted image 20250112170746.png]]
![[Pasted image 20250112170902.png]]

Paling commong sekarang 802.11ac. ax itu bedanya gk jaduh sama ac dan lebih mahal. Jadi blom waktunya ganti.

#### PENTING, BEDANYA 2.4GHZ TO 5GHZ
![[Pasted image 20250112171016.png]]
2.4ghz itu default in most cases. Jadinya suka crowded. Semuanya pake frekuensi itu.

5Ghz lebih less crowded. Bahkan sekarang 6GHz udah ada, lebih gk crowded lagi.

**2.4ghz juga much slower dari pada 5ghz.**

**2.4ghz tapi better coverage, it goes through concrete better. kalo 5ghz jaraknya gk sejauh itu dan lebih sulit nembus tembok. 6ghz sama juga, lebih kecil coveragenya dari 5ghz tapi lebih cepet.**

![[Pasted image 20250112171354.png]]

1 Access point can have multiple SSID (Nama Wifinya, Service Set Identifier).

![[Pasted image 20250112171454.png]]

**SS vs SSID**
![[Pasted image 20250112171529.png]]

SS -> Devices dalam 1 network wifi itu
SSID -> Nama wifinya.

**WEP, (Wired Equivalent Privacy) - Gk secure**
![[Pasted image 20250112171625.png]]

WPA2 dan WPA3 adalah standar sekarang.

![[Pasted image 20250112171654.png]]

Yang recommended sekarang itu WPA3.

WPA1 --> Pake RC4 dan TKIP, udah gk secure
WPA2 --> Paling banyak dipake, masih secure asal pake AES. Kalo diset pake TKIP gk secure. Pake pre-set key.
WPA3 --> 2020, Stronger, pake Simultaneous Authentication of Equals (SAE). Pake AES-256 in GCP mode with SHA-384 as HMAC. Segala data yang disent dari access point itu encrypted with a specific key yang cuma kita yang bisa decrypt.  

WPA bisa ada account lockout buat mencegah brute-force

### Bluetooth
![[Pasted image 20250112172034.png]]
Short-rage. Pake 2.4Ghz. PAN (Personal Area Network)

Bluetooth bisa menjanggau 100 meters kalo Class 1.

![[Pasted image 20250113012218.png]]
![[Pasted image 20250113012241.png]]

## Wireless Network
![[Pasted image 20250113012451.png]]

Li-Fi -> Pake Cahaya. 100 Gigabits. And it can use different types of light to send reasonably fast internet.

Zigbee -> Personal Area Network range. 10-100m. Low speed.

![[Pasted image 20250113012611.png]]

### Cellular Network
![[Pasted image 20250113012737.png]]
![[Pasted image 20250113012814.png]]

Range 5G itu gk terlalu jauh. Cuma 500meter dari antena coveragenya.. baru tw. Kyk yg wifi, lebih kecil coveragenya tapi lebih cepat.

Gila 4G 10 miles radius.

![[Pasted image 20250113013021.png]]
Li-Fi most secure karena pake cahaya.
![[Pasted image 20250113013113.png]]
Ini harus cek tabel sih. Keknya harus diafal.
![[Pasted image 20250113013212.png]]

### L1 - L3 Networking Devices on OSI Model
![[Pasted image 20250113113434.png]]
![[Pasted image 20250113113543.png]]

**Inget, some switches can use IP (L3 Switch).**

![[Pasted image 20250113113759.png]]
![[Pasted image 20250114143017.png]]
VXLAN itu buat yg besar bgt, kyk AWS, Google, Azure, etc.

![[Pasted image 20250114143057.png]]

![[Pasted image 20250114143240.png]]

### Layer 3 Routing Protocol
![[Pasted image 20250114143535.png]]
![[Pasted image 20250115132239.png]]
**Distance vector routing protocols (cuma calculate jarak, gk itung bandwidth):**
- RIP --> Cuma ambil jarak terdekat. Hop terdikit. Tapi gk efektif karena gk ngitung bandwidthnya.

![[Pasted image 20250115132355.png]]

![[Pasted image 20250115132506.png]]
**Link-state routing protocols (memperhitungkan jarak dan bandwidth juga, jadi lebih akurat):**
- OSPF
- BGP (Border Gateway Protocol) --> ISP sekarang mostly pake ini
![[Pasted image 20250115132651.png]]


### Network Performance and Traffic Management
![[Pasted image 20250115151437.png]]
![[Pasted image 20250115151501.png]]
![[Pasted image 20250115151644.png]]
![[Pasted image 20250115151806.png]]
![[Pasted image 20250115151952.png]]

## Firewalls

##### Packet Filtering Firewalls
![[Pasted image 20250116213145.png]]

##### Stateful filtering firewalls
![[Pasted image 20250116221019.png]]
--> Kalo connection udah established, jadi allowed.

So in my example here, I have an internal workstation with the IP of 100.1.1.1 going to an external web server, since it's accessing the web server on Port 443, or Https. Well then the connection is allowed. Once that connection is established, the firewall writes a state table entry saying that that socket pair, meaning those source and destination IPs and ports are allowed to communicate with each other.

So when the actual web server sends traffic back, it's allowed through the firewall because we establish that session.

Bisa di DoS.

##### Proxy Server, Application Firewall, Network Firewall, Host-based Firewall
![[Pasted image 20250116223822.png]]

WAF, layer 7.

##### Next Generation Firewall (NGFW)
![[Pasted image 20250116224021.png]]
Ada deep packet inspection (IDS/IPS)

##### Bastion Host and Dual-Homed Host
![[Pasted image 20250116224100.png]]

![[Pasted image 20250116225548.png]]

![[Pasted image 20250116225625.png]]

Firewall kalo bisa internal dan external beda merek. Misalnya depannya Cisco, dalamnya Juniper. Jadi kalau ada CVE di yang 1, gk jebol semua.

![[Pasted image 20250116225721.png]]

### Modem (Modulator / Demodulator)
![[Pasted image 20250116225817.png]]

![[Pasted image 20250116231136.png]]
DTE dan DCE (Modem) itu jaman dulu. Jaman dulu mesti make 2 kotak, DTE dan DCEnya.

![[Pasted image 20250116231410.png]]

Fail-secure --> Meskipun dia fail, tetep secure. Contoh: Firewall, kalo rusak, langsung deny all traffic. Meskipun rusak, kita tetep secure.

**Fail-secure** is a design principle for systems and devices that ensures security is maintained in the event of a failure or malfunction


## Securing Data In Motion
![[Pasted image 20250116231655.png]]
PAP --> Kyk HTTP Basic Auth

![[Pasted image 20250117011307.png]]
CHAP --> Pake preshared password. Jadi gk disendthrough network, tapi masalahnya passwordnya distore dalam plaintext.


EAP --> Extensible Authentication Protocol (Penting)

![[Pasted image 20250117011342.png]]
![[Pasted image 20250117011426.png]]

SLIP and PPP
![[Pasted image 20250117011545.png]]

VPN
![[Pasted image 20250117011555.png]]
--> Awesome

PPTP (Old, and have many issues, pake VPN aja) and L2TP (On Layer 2 of the OSI model)
![[Pasted image 20250117011721.png]]

#### IPSEC (PENTING FOR EXAM)
![[Pasted image 20250117011738.png]]
VPN pake IPSEC. IPSEC itu end to end encryption.

**IPSEC is a set of protocols that provide a cryptographic layer to IP traffic, both for IPV4 and IPV6.**

**On IPV4, it's something that's tagged onto the protocol. In IPV6, it's designed in.**

**And one of the places where you might use IPsec would be when you use a VPN.**

**SA (Security Association)** --> Simplex, one way. Used to negotiate ESP (Encapsulating Security Payload) or AH (Authentication Header)

**ISAKMP (Internet Security and Key Management Protocol)** --> Manages SA creation process

**Tunnel Mode --> Encrypt semuanya termasuk headernya** (MOST COMMON)
**Transport Mode --> Cuma Encrypt dan authenticate payloadnya aja.**

**IKE (Internet Key Exchange)** --> Negotiates the algorithm selection process. Negotioate the symmetric encryption and the Hash. Dia pilih yang paling cepet dan paling secure 

![[Pasted image 20250117012229.png]]

ISDN and DSL
![[Pasted image 20250117012416.png]]

**Callback and Caller ID**
![[Pasted image 20250117012551.png]]
![[Pasted image 20250117225029.png]]
![[Pasted image 20250117225243.png]]
Thin client, Zero client, Thick client

Instant Messaging
![[Pasted image 20250117225555.png]]

Signal --> Salah satu most secure instant messaging app in regards collecting sensitive attachments and mining customer data.

![[Pasted image 20250117225752.png]]

![[Pasted image 20250117225939.png]]
![[Pasted image 20250117230102.png]]


# Domain 5  - IAM (Identity and Access Management)

### Access Control
![[Pasted image 20250117232642.png]]
IAAA --> Identify, Authenticate, Authorize, and Accountable


![[Pasted image 20250119020845.png]]

Penting tuh something **you know (Type 1), you have (Type 2), dan you are (Type 3)**.

### Type 1 Authentication - Something you know
![[Pasted image 20250119021152.png]]
--> Ini tipe yang paling lemah karena paling gampang dicompromise, e.g: Password.

![[Pasted image 20250119024416.png]]
- Password harus ada kapital, letter, special chars.
- Password harus selalu dirotate.
- Gk boleh pake 12-24 password sebelumnya at least.
- Password ada expirynya.
- Gk boleh ganti-ganti password terus menerus sampe bisa pake 12 password sebelumnya loll. Harus ada cooldown boleh ganti password at least 5 hari. Unless pwnya langsung jebol.

![[Pasted image 20250119024556.png]]
![[Pasted image 20250119024703.png]]
![[Pasted image 20250119024744.png]]
![[Pasted image 20250119024815.png]]
**Clipping Levels** --> To prevent administrative overhead. (boleh multiple entry sebelum lockout, karena bisa aja typo. Misalnya maksimal 3-5x typo)

![[Pasted image 20250119025021.png]]

### Type 2 Authentication - Something you have (Possession factor)
![[Pasted image 20250119025056.png]]
![[Pasted image 20250119151058.png]]

Singe-use password itu something you have, bukan you know.
![[Pasted image 20250119151212.png]]
![[Pasted image 20250119151314.png]]
KlikBCA
![[Pasted image 20250119151354.png]]
MicroChip di-implant --> akan jadi popular beberapa tahun ke depan.

### Type 2 Authentication - Something you are
- Iris, biometrics, finger print, face.
- Most secure, but most expensive. Iris scanner, fingerprint scanner, face scanner.

![[Pasted image 20250119151450.png]]
![[Pasted image 20250119151529.png]]
--> Penting buat atur sensitivitynya.
![[Pasted image 20250119151755.png]]
Physiological --> Facial recognition, palm veins, hand geometry, etc.
Behavioral --> How you walk, your signature, etc.

Hati-hati di EU, privacynya by collecting biometrics.

![[Pasted image 20250119151859.png]]
Bahaya Biometrics --> If you lose it, you can't get a new one. Kalo muka lu diprint 3d, udah lah jebol. Kalo sidik jarilu dicuri, kacau. 

![[Pasted image 20250119151955.png]]

## Authorization
--> Memberikan aksesnya.
![[Pasted image 20250119152058.png]]
--> Access controlnya, rolenya apa.
![[Pasted image 20250119152133.png]]
Discretionary access control (DAC) is ==a cybersecurity system that allows the **owner of an object to decide who can access** it and what they can do with it==. DAC is based on Access Control Lists (ACLs).

DAC --> When availability is priorty


**Mandatory Access Control (MAC**) is ==a security system that limits user access to data based on **predefined rules**==. It's used to protect sensitive information in environments that require a high level of security.

MAC --> When Confidentiality is priority

**RBAC (PENTING)**
![[Pasted image 20250119215124.png]]
--> Need-to-know

**ABAC (Lebih secure, dan lebih granular, slowly moving to this dari RBAC)** 
![[Pasted image 20250119215306.png]]
--> Sama kyk RBAC tapi ada environmental conditions. 
--> Policy based

**Context-Based and Content-Based (bagian dari ABAC)**
![[Pasted image 20250119215929.png]]

## Accountability / Auditing
![[Pasted image 20250119220039.png]]
--> Non-repudiaton.

### Access Control Systems
![[Pasted image 20250119220153.png]]




















































































































































