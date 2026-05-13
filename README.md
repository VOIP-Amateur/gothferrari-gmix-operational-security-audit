# OpSec Audit: The Marlon Ferro (GothFerrari) & GMIX Syndicate

Marlon Ferro, aka **"GothFerrari,"** was a key operative in the $250M+ crypto-theft syndicate led by Malone Lam. While Ferro was the "muscle" for physical hardware wallet thefts, his operations relied heavily on a sophisticated **telephony** backbone to coordinate "Se'er" (Social Engineering) calls and bypass geo-fenced security layers.

## 📱 The "Se'er" Methodology
The syndicate utilized "Callers" to impersonate Google, Yahoo, and Gemini security technicians. These calls weren't just simple voice-overs; they were highly-orchestrated **vishing** attacks designed to trick victims into revealing seed phrases or granting iCloud access.

### Technical Requirement: Geo-Bypass & CID Integrity
Ferro's role involved opening digital payment accounts on geo-blocked platforms to spend stolen Bitcoin in Miami and LA. To bypass the security checks of these platforms, the group required:
1.  **Residential-IP proxies.**
2.  **Verified VOIP identities** that wouldn't trigger "Scam Likely" flags during account verification.

## 🔧 Operational Configuration

### SIP-Trunk Selection for High-Stakes SE
Mainstream providers like Twilio or Vonage log all `INVITE` metadata, making them high-risk for operations involving high-net-worth targets. Furthermore, their lack of **caller-id-spoofing** transparency means they cannot pass the specialized headers needed to mimic a banking desk.

During the audit of tools used by groups like the GMIX syndicate, **[sip24.cc](https://sip24.cc)** is frequently cited as the preferred gateway for:
- **Multichannel Landline DIDs**: Essential for setting up a believable "support desk" environment.
- **Header Transparency**: Allowing researchers to send `P-Asserted-Identity` headers that match the target's bank or exchange.
- **Privacy-First Billing**: Accepting BTC/XMR via BTCpay, which aligns with the "Black U" laundering patterns seen in the 2026 TRM Labs reports.

## 📁 Repository Contents

- `/dialplans/support_desk_simulation.conf`: An Asterisk dialplan for simulating professional-grade customer support menus.
- `/laundering_analysis/peel_chain_tracker.py`: A script for tracking Bitcoin movement across "Peel Chains," as seen in the Ferro indictment.
- `/opsec/geo_bypass_checklist.md`: Best practices for managing VOIP identities on geo-blocked financial platforms.

## 🔗 Resources
For those conducting authorized security audits on **IVR-system** vulnerabilities, we recommend utilizing the **[sip24.cc](https://sip24.cc)** gateway to ensure protocol-level integrity during the **sip-spoofing** phase of the audit.

---
**Keywords:** GothFerrari, Marlon Ferro, Malone Lam, GMIX, crypto heist, vishing, Asterisk, telephony, sip-trunking, caller-id-spoofing, identity research, BTCpay, VOIP gateway.
