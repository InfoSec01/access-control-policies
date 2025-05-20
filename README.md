<div align="center">
  <h1>🔐 Information Security Protocols Lab: Access Control & Network Defense</h1>
</div>

Welcome to my **Information Security Protocols** lab — a real-world simulation of access control and perimeter defense using industry-grade tools across a multi-VM Linux environment.

This project demonstrates how I implement **authentication**, **authorization**, **network security**, and **intrusion detection** to build a resilient security architecture—just like in modern enterprise environments.

---

## 📁 Contents

1. [🛂 LDAP & Kerberos Authentication](#ldap--kerberos-authentication)
2. [🔥 Host-Based Firewall (firewalld)](#host-based-firewall-firewalld)
3. [🛡️ Web Application Firewall (ModSecurity + OWASP CRS)](#web-application-firewall-modsecurity--owasp-crs)
4. [🚨 Intrusion Detection System (Snort)](#intrusion-detection-system-snort)
5. [📸 Screenshots](#screenshots)
6. [🎯 Why This Matters](#why-this-matters)
7. [🚀 Let’s Work Together](#lets-work-together)

---

## 🛂 LDAP & Kerberos Authentication

Centralized authentication is critical in any secure environment.

- ✅ Set up **OpenLDAP server** for directory-based identity management.
- ✅ Integrated **Kerberos** for secure, ticket-based authentication.
- ✅ Configured Linux clients to authenticate against LDAP/Kerberos.
- ✅ Tested with login scenarios and access restrictions.

**Tools Used:** `slapd`, `krb5kdc`, `kadmin`, `sssd`, `pam_krb5`

> 🧠 *Why this matters:* Centralized authentication ensures secure and scalable identity management across large infrastructures.

## 📸 Screenshots

<img src="https://github.com/InfoSec01/information-security/blob/main/ldap-installed.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/ldap-shadow-password.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/ldap-config-output.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/kerberos-config.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/kerberos-principles.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/kerberos-principles1.png" width="50%"/>

---

## 🔥 Host-Based Firewall (firewalld)

Protecting the network starts at the host level.

- 🔒 Configured `firewalld` zones to restrict traffic based on services.
- ✅ Allowed only essential ports (SSH, HTTP, DNS, Kerberos).
- 🚫 Blocked all unauthorized connections and verified using port scans.

**Tools Used:** `firewalld`, `firewall-cmd`, `nmap`, `ss`

> 🧠 *Why this matters:* Host firewalls prevent lateral movement and provide the first line of defense against unauthorized access.

## 📸 Screenshots

<img src="https://github.com/InfoSec01/information-security/blob/main/apache2-installed-testing.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/firewalld-config.png" width="50%"/>

---

## 🛡️ Web Application Firewall (ModSecurity + OWASP CRS)

Hardened the Apache web server against web attacks.

- ⚙️ Installed and enabled **ModSecurity** on Apache.
- 🧰 Deployed **OWASP Core Rule Set (CRS)** for defense against:
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - CSRF, RFI, LFI, and more
- 🧪 Tested with malicious payloads and confirmed blocked attacks.

**Tools Used:** `apache2`, `modsecurity`, `OWASP CRS`, `curl`, `Nikto`

> 🧠 *Why this matters:* A WAF guards web-facing applications—your business's most exposed assets.

## 📸 Screenshots

<img src="https://github.com/InfoSec01/information-security/blob/main/modsecurity-config.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/modsecurity-enabled-security2module.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/owasp-corerule-download-latestrelease.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/owasp-corerule-config.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/owasp-corerule-configured-output.png" width="50%"/>

---

## 🚨 Intrusion Detection System (Snort)

Monitored network activity for suspicious behavior and threats.

- 🔍 Installed and configured **Snort** in IDS mode.
- 📈 Tuned Snort rules to detect port scans, brute-force attacks, and malware patterns.
- 📧 Integrated alerting to notify on suspicious traffic.

**Tools Used:** `snort`, `tcpdump`, `Wireshark`, `barnyard2`

> 🧠 *Why this matters:* An IDS offers critical visibility into network anomalies and breach attempts.

## 📸 Screenshots

<img src="https://github.com/InfoSec01/information-security/blob/main/snort-installed-active.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/snort-config.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/snort-ruleset-test.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/snort-traffic-output.png" width="50%"/>
<img src="https://github.com/InfoSec01/information-security/blob/main/snort-file-analysis.png" width="50%"/>

---

## 🔒 Cryptography (AES, OpenSSL, Hashing, HMAC)

Secured sensitive data using encryption and message authentication.

### 🔑 AES Encryption with acescript
- Custom bash script `acescript` for AES-256-CBC encryption and decryption.
- Used for securing backup archives and sensitive config files.

### 📸 Screenshots

<img src="" width="50%"/>
<img src="" width="50%"/>

---

### 🧪 OpenSSL & HMAC

- Generated **symmetric and asymmetric keys** using OpenSSL.
- Signed and verified files using **HMAC with SHA-256** for message integrity and authenticity.

### 📸 Screenshots

<img src="" width="50%"/>
<img src="" width="50%"/>

---

### 🧮 Hashing

- Verified file integrity using:
  - `sha256sum`
  - `md5sum`

### 📸 Screenshots

<img src="" width="50%"/>
<img src="" width="50%"/>

---

### 🎯 Why This Lab?

This lab demonstrates how I apply industry-standard protocols to secure Linux environments:

- 🔐 **Centralized authentication** improves access control and auditability.
- 🌐 **Network perimeter defense** detects and blocks real-time threats.
- 🔒 **Cryptography** ensures data confidentiality, integrity, and authenticity.

---

### 📬 Contact Me

Feel free to connect if you're looking for someone who can build, secure, or audit Linux-based systems using open-source security tools.

**📧 Email:** baratulkhan@gmail.com
