
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
--> By default unreasonable search and seizure itu illegal by the US Government. **UNLESS, there's an immediate threat to human life or of evidence destruction.**













































