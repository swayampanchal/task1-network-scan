
# Phishing Email Analysis

## What is Phishing?
Phishing is a cyber attack method used by attackers to trick users into revealing sensitive information such as login credentials, credit card details, or installing malware. It often appears to be from a trusted source, but the true intention is malicious.

## Sample Email Description:
- **Subject**: 🚨 Urgent Action Required: Your Microsoft Account Will Be Locked
- **From**: Microsoft Support <admin@micr0soft-support.com>
- **To**: victim@yourdomain.com
- **Date**: Wed, 07 Aug 2025 10:42:50 +0530

---

## Phishing Indicators Found:

### 1. Suspicious Sender Address
- The email address is `admin@micr0soft-support.com`
- Real Microsoft email domains use `@microsoft.com`
- The spoofed domain uses a zero "0" instead of the letter "o" – a common tactic in phishing


### 2. Header Issues (from MXToolbox)
- Return-Path and Reply-To domains are spoofed
- Mail server IP is from `192.168.1.25`, a private, fake network IP
- Mail relay shows it was sent from a suspicious and likely fake domain


### 3.  Link Mismatch
- Button says: “Verify Now”
- Likely hidden behind a suspicious domain (not visible here, but assumed from pattern)

### 4.  Spelling/Grammar Issues
- Generic greeting (“Dear User”), no personalization
- Urgent tone, bad formatting, overly alarming language

### 5. Social Engineering Techniques
- Creates panic using terms like “urgent” and “account will be locked”
- Pushes user to act quickly without verifying authenticity

---

## Conclusion
This is a phishing email designed to look like a legitimate message from Microsoft. The sender domain is spoofed, email headers reveal a fake origin server, and the email uses urgency and fear to manipulate the recipient.

Users should be educated to recognize these signs and avoid clicking any links or replying.

---

## Tools Used:
- **MXToolbox Email Header Analyzer**: https://mxtoolbox.com/EmailHeaders.aspx
- **Hunter.io Email Verifier**: https://hunter.io/email-verifier
- **Email Client (Simulated)** and basic Markdown editor
