> Above every possessor of knowledge is a Knower

# 🤝 Contributing to Hadak

First — understand this:

> This is not a typical app.
> This is a **privacy-first, fully decentralized system built in the open**.

If you’re here to help, you’re stepping into a system that must remain:
* **Trustless:** No reliance on any single entity.
* **Serverless:** Pure P2P infrastructure.
* **Observable:** Auditable by everyone, including adversaries.

---

## 🧭 Project Principles (Non-Negotiable)

Before contributing, you must align with these:

* **No Centralization:** No servers, no fallback APIs, no "master" nodes.
* **No Tracking:** Zero analytics, zero telemetry, zero "usage reporting."
* **User Sovereignty:** The user owns all data. Nothing leaves the device unencrypted.
* **Security over Convenience:** We will take the harder path if it protects the user.
* **Simplicity over Cleverness:** Code must be readable to be auditable.

---

## 🧱 Architecture & Tech Stack

* **Language:** Python 3 (Unified across the stack).
* **Platform:** Mobile-first (Kivy / Buildozer / Android / iOS).
* **Network:** P2P / DHT-based (e.g., NKN SDK).
* **Storage:** Local-only, encrypted (PBKDF2/Salted Hashing).
* **Concurrency:** Non-blocking/Asynchronous (Must not lock the UI thread).

---

## 🧩 The "Hard Problems"

We are actively seeking experts to tackle these specific architectural challenges:

1.  **Location Obfuscation:** Sharing "nearby" service data without exposing high-precision GPS coordinates to the peer network.
2.  **Sybil Resistance:** Maintaining a healthy DHT without a central authority to verify identities.
3.  **Metadata Hardening:** Minimizing the "digital footprint" left by P2P message routing.
4.  **Supply Chain Integrity:** Ensuring the build process is reproducible and free from library injections.

---

## 🛠️ Ways You Can Contribute

### 1. Security & Cryptography (Highest Priority)
* Audit encryption flows and key management.
* Improve forward secrecy and E2EE implementations.
* Analyze attack surfaces and propose hardening measures.

### 2. Distributed Systems
* Optimize peer discovery and message routing efficiency.
* Improve fault tolerance for high-latency or intermittent mobile networks.

### 3. Documentation & Safety
* Draft **Threat Models** for specific features.
* Simplify complex P2P concepts for non-technical users without hiding the truth.

---

## 🚫 What NOT to Contribute

Do **NOT** propose or submit:
* Centralized APIs or cloud-sync features.
* Analytics, Ads, or Monetization hooks.
* Heavy external dependencies without a security justification.
* Closed-source "black box" components.

---

## ⚙️ Development Guidelines

### 1. Security First
Assume your code will be inspected by attackers and your logic will be abused. Write "defensive" code.

### 2. Dependency Protocol
* Minimize external libs.
* Every new dependency requires a `pip-audit` or safety scan.
* Prefer Python standard libraries wherever possible.

### 3. Performance
On mobile, battery is a constraint. Contributions to the networking layer must be optimized for low power consumption.

---

## 🔐 Rules for Sensitive PRs (Crypto/Networking)

For any change to the **Encryption, Key Management, or P2P layer**, you must:
1.  **Describe the Design:** Explain the "Why" and the "How."
2.  **State Assumptions:** What must be true for this code to be safe?
3.  **Identify Attack Vectors:** What are the known trade-offs or remaining risks?

*PRs in these areas without a written design summary will be closed.*

---

## 🧵 Pull Request Process

1.  **Fork & Branch:** Keep PRs small and focused on a single issue.
2.  **Verify Integrity:** Ensure the code passes all local linting (PEP8).
3.  **No "Coolness" Reviews:** We don't care if a solution is "cool"; we care if it is resilient and simple.

---

## 🧠 Mindset

This project is not about scaling fast or chasing a high user count. It is about building a system that survives real-world pressure and remains standing when centralized systems fail.

**By me or others, this is the future. We have the opportunity to do the right thing.**

If you believe in decentralized sovereignty, we welcome your eyes and your hands.

> **Final Note:** We are developing in front of everyone. Safety is achieved through transparency, not obscurity. In Shaa Allah, we will build a system that truly serves.
