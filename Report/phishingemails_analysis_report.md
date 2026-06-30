# Phishing Emails Analysis Report:
# ->Sample Email 1:
-> Subject: [EXTERNO] Reunião / Custos dos Consignados
-> Findings:
- SPF: Passed 
- DKIM: Passed
- DMARC: Passed 
- Email traveled through Google's mail servers.
- No spoofing detected.
- Sender domain matched authentication records.
- No suspicious routing observed.
-> Conclusion:
- This email appears to be legitimate because all major email authentication mechanisms (SPF, DKIM, and DMARC) passed successfully. The routing path is consistent with Google's infrastructure, indicating that the sender's identity was successfully verified.

# ->Sample Email 2:
-> Subject: Attention: I am Diplomatic Agent Mr. Wood Forest
-> Findings:
- SPF: Failed
- DKIM: None
- DMARC: None
- Sender IP: 109.202.24.52
- HELO server: 54upr.rosreestr.ru
- From: postfiji.com.fj
- Reply-To: mywoodforestbiz.7@gmail.com
- Outlook marked:
    CompAuth = Fail
    SCL = 5
    (Spam)
-> Suspicious Indicators:
- SPF authentication failed.
- No DKIM signature.
- No DMARC policy.
- Reply-To address is completely different from sender domain.
- Classic advance-fee/"millions of dollars" scam.
- Fake diplomatic delivery story.
- Sender server does not belong to the claimed organization.
-> Conclusion:
- This email is highly suspicious and exhibits multiple phishing indicators. Authentication checks failed, the sender attempted to impersonate a legitimate organization, and the content uses social engineering involving a large sum of money to manipulate the recipient. The email should be treated as malicious.

# ->Sample Email 3:
-> Subject: Hi
-> Findings:
- SPF: SoftFail
- DKIM: None
- DMARC: None
- Sender IP: 202.129.206.234
- From: shore@suksapan.or.th
- Reply-To: elizabethray993@gmail.com
- Outlook marked:
    CompAuth = Fail
    SCL = 5
    (Spam)
-> Suspicious Indicators:
- SPF SoftFail indicates the sending server is not fully authorized.
- No DKIM signature.
- No DMARC policy.
- Reply-To points to a Gmail account instead of the sender's domain.
- Subject is vague ("Hi").
- Body requests assistance with handling inherited funds.
- Uses emotional manipulation (cancer, deceased husband, urgent timeframe).
- Typical advance-fee/social engineering scam.
-> Conclusion:
-This email is a phishing attempt that relies on emotional manipulation to convince recipients to respond. Authentication mechanisms are weak or absent, the Reply-To address differs from the sender's domain, and the email content matches common financial scam techniques. It should be classified as malicious.
