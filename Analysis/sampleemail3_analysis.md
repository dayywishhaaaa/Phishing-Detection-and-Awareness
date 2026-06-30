#  Sample Email 3 Analysis:
-> Email Type: Phishing / Advance Fee Fraud (High Risk)

#  Subject Analysis:
- Subject: Hi
-> Observation: The subject is extremely generic and provides no meaningful information. Attackers often use vague subjects to encourage recipients to open the email out of curiosity.
-> Indicator: Generic Subject Line

#  Sender Analysis:
- From: shore@suksapan.or.th
- Reply-To: elizabethray993@gmail.com
-> Finding:
- The sender claims to be from the domain: suksapan.or.th
- However, replies are redirected to a personal Gmail account.
- This mismatch is a strong phishing indicator because legitimate organizations generally use the same domain for both sending and replying.
-> Indicator: Reply-To Mismatch

#  SPF Analysis:
- Header shows:
Received-SPF: SoftFail
Authentication-Results:
spf=softfail
-> Meaning:
- Unlike Sample 2, this is a SoftFail, not a complete Fail.
- A SoftFail means the domain owner has indicated that the sending server probably isn't authorized, but the receiving server may still accept the message.
- The sending IP was: 202.129.206.234  which is discouraged from sending mail on behalf of: suksapan.or.th
-> Indicator: SPF SoftFail

#  DKIM Analysis:
- Header states: dkim=none
-> Meaning:
- The email is not digitally signed.
- There is no way to verify that it has not been modified.
-> Indicator: Missing DKIM

#  DMARC Analysis:
- Header states: dmarc=none
-> Meaning:
- The domain has no DMARC policy.
- This allows spoofed emails to bypass an important security control.
-> Indicator: Missing DMARC

#  Return Path:
- Return-Path: shore@suksapan.or.th
-> Although it matches the From address, authentication still fails because SPF SoftFail and CompAuth fail indicate the message cannot be trusted.

#  Sending Server:
- The originating server is host4.ns.co.th
- The actual client IP shown earlier is 102.69.133.254
- The email passed through host4.ns.co.th before entering Microsoft's mail infrastructure.
- While the server itself may not necessarily be malicious, the authentication failures and phishing content make the email suspicious.

#  Sender IP:
202.129.206.234
- This IP is reported in the SPF results as not being an authorized sender. Combined with the SoftFail result, this lowers trust in the message.

#  Email Content Analysis:
- The email says: "Proposal: Partnership for Allocated Funds..."
-> It claims:
- the sender has cancer
- wants help transferring money
- inherited funds from a deceased husband
- asks the recipient to reply
-> This is another classic Advance Fee Fraud (419 Scam).

#  Social Engineering Techniques:
-> This email uses several manipulation tactics:
- ✔ Emotional appeal (claims terminal illness)
- ✔ Sympathy
- ✔ Promise of financial reward
- ✔ Curiosity
- ✔ Urgency ("limited timeframe")
-> These techniques are commonly used to manipulate victims into responding.

#  HTML Content:
-> Unlike Sample 2, this email contains:
- multipart/alternative, with both: Plain text version and HTML version
-> Attackers often include HTML emails because they allow:
- clickable links
- formatting
- hidden content
- embedded tracking
-> Indicator: HTML Email Format

#  Overall:
Indicator              |        Status
SPF                    |	⚠️ SoftFail
DKIM                   |	❌ Missing
DMARC                  |	❌ Missing
Reply-To mismatch      |	❌ Yes
Emotional manipulation |	❌ Yes
Financial scam         |	❌ Yes
Generic subject        |	❌ Yes
HTML email             |	⚠️ Yes
Social engineering     |	❌ Yes
#  Risk Level:

🔴 High Risk – Confirmed Phishing / Advance Fee Scam

#  Recommended Action:
- Do not reply.
- Do not click any links (if present).
- Do not provide personal or financial information.
- Report the email as phishing.
- Delete the message.
