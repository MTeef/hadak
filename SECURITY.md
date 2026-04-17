
# 🔐 Security Manifest — Hadak (Ligita)

## Our Premise

Hadak is built on a simple but strict principle:

> **User data must never leave the user’s control.**

This is not just a feature — it is a constraint that shapes every
technical decision.

---

## 🧱 Core Constraints

We intentionally operate under the following constraints:

* **Language:** Python (unified across the entire system)
* **Architecture:** Fully decentralized (P2P / DHT-style)
* **Storage:** All data remains **on-device only**
* **Encryption:** All sensitive data is encrypted locally and in transit
* **Business Model:**

  * No ads
  * No tracking
  * No data monetization
  * No central servers

---

## 🌍 Open Development Reality

We are building this system **in public**.

That means:

* Anyone can inspect the code
* Anyone (including adversaries) can study the system
* Security cannot rely on secrecy

This leads to our core belief:

> **Security must be resilient even when fully exposed.**

---

## ⚠️ Threat Model (What We Assume)

We explicitly assume:

* Malicious users can run modified clients
* Network traffic can be observed and replayed
* Adversaries may attempt:

  * Message interception
  * Traffic analysis
  * Identity spoofing
  * Resource abuse (spam, flooding)
  * Supply chain attacks

We do **not** assume trusted infrastructure.

---

## 🔐 Security Layers Overview

### 1. Identity & Key Ownership

* Each node generates its own cryptographic identity
* No centralized identity provider
* Private keys never leave the device

---

### 2. End-to-End Encryption

* Session-based encryption using symmetric keys (e.g. AES-GCM)
* Secure key exchange using asymmetric cryptography
* Messages are encrypted **before entering the network**

---

### 3. Transport Resilience

* Messages propagate through a distributed network (inspired by systems like NKN)
* Intermediate nodes cannot read message contents
* No central routing authority

---

### 4. Data Minimization

* No raw location storage
* No global user profiles
* No behavioral tracking

---

### 5. Local-Only Data Model

* All application data:

  * Stored locally
  * Encrypted at rest
* No backend database exists to breach

---

## 🧨 Supply Chain & Code Integrity Risks

We recognize that in a Python-based, open system, **supply chain attacks are one of the biggest risks**.

### Our concerns include:

* Malicious or compromised dependencies
* Dependency confusion attacks
* Hidden backdoors in third-party libraries
* Unsafe updates

---

## 🛡️ Mitigation Strategies (Current & Planned)

### 1. Dependency Control

* Prefer **minimal external dependencies**
* Audit all libraries before inclusion
* Pin exact versions (no floating dependencies)

---

### 2. Reproducible Builds (Planned)

* Ensure builds can be verified independently
* Detect tampering between source and distributed binaries

---

### 3. Code Transparency

* Fully open-source codebase
* Public review encouraged
* No obfuscated or hidden logic

---

### 4. Cryptographic Boundaries

* Sensitive operations isolated and auditable
* Avoid “magic” abstractions in crypto logic

---

### 5. Runtime Safeguards (Planned)

* Integrity checks for critical modules
* Detection of unexpected code injection

---

### 6. Principle of Simplicity

> Complexity is the enemy of security.

We intentionally:

* Avoid unnecessary layers
* Avoid hidden automation
* Keep flows understandable and auditable

---

## 🔍 What We Need Help With

We actively invite security researchers, engineers, and reviewers to help us harden:

### Critical Areas:

* Key exchange design (forward secrecy improvements)
* Traffic analysis resistance
* Metadata leakage (timing, frequency, patterns)
* Peer discovery safety
* Spam and abuse resistance in a P2P system
* Secure update mechanisms
* Dependency auditing strategies

---

## 🚫 What We Avoid by Design

* Centralized logging
* User tracking systems
* Behavioral analytics pipelines
* Server-side data storage
* “Trust us” security models

---

## 🤝 Responsible Disclosure

If you discover a vulnerability:

* Please report it responsibly
* Give us time to fix before public disclosure

(Disclosure process to be defined — coming soon)

---

## 🧠 Philosophy

Hadak is not trying to be “perfectly secure.”

It is trying to be:

> **Minimally trusted, maximally transparent, and resilient under exposure.**

---

## ⚡ Final Note

We are building:

* In public
* Under constraints
* Against real-world adversaries

If something looks weak — it probably is.

**Tell us. Break it. Help us fix it.**
