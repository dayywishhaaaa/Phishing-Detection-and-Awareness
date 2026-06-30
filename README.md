# Phishing Detection and Awareness: 
## Overview
- This project focuses on analyzing email headers to identify phishing attempts using industry-standard email authentication mechanisms. Three email samples were examined to distinguish legitimate emails from phishing emails based on header analysis, authentication results, routing information, and social engineering indicators.

## Objectives

- Analyze raw email headers
- Verify SPF, DKIM, and DMARC authentication
- Examine email routing using Received headers
- Identify spoofing and phishing indicators
- Classify emails as legitimate or malicious
- Document findings in a professional report

## Tools Used

- Kali Linux
- Google Admin Toolbox – Message Header Analyzer
- MXToolbox – Email Header Analyzer
- Git & GitHub
- Public phishing email datasets

## Project Structure

```
Phishing-Detection/
│   
├── Analysis
│   ├── sampleemail1_analysis.md
│   ├── sampleemail2_analysis.md
│   └── sampleemail3_analysis.md
├── Evidence
│   ├── Headers
│   │   ├── sampleemail1_rawheader.html
│   │   ├── sampleemail2_rawheader.html
│   │   └── sampleemail3_rawheader.html
│   ├── Screenshots
│   │   ├── sampleemail1_headeranalysis_googletoolbox.png
│   │   ├── sampleemail1_headeranalysis_mxtoolbox.png
│   │   ├── sampleemail2_headeranalysis_googletoolbox1.png
│   │   ├── sampleemail2_headeranalysis_googletoolbox2.png
│   │   ├── sampleemail2_headeranalysis_mxtoolbox.png
│   │   ├── sampleemail3_headeranalysis_googletoolbox1.png
│   │   ├── sampleemail3_headeranalysis_googletoolbox2.png
│   │   └── sampleemail3_headeranalysis_mxtoolbox.png
│   └── URLs
├── Report
│   └── phishingemails_analysis_report.md
├── Samples
│   ├── sampleemail1.eml
│   ├── sampleemail2.eml
│   └── sampleemail3.eml
└── README.md
```

## Analysis Summary

-> Sample 1
- SPF: Pass
- DKIM: Pass
- DMARC: Pass
- Classification: Legitimate

-> Sample 2
- SPF: Fail
- DKIM: None
- DMARC: None
- Multiple spoofing indicators
- Reply-To mismatch
- Classified as Phishing

-> Sample 3
- SPF: SoftFail
- DKIM: None
- DMARC: None
- Reply-To mismatch
- Social engineering content
- Classified as Phishing

## Key Phishing Indicators Identified

- SPF authentication failure
- Missing DKIM signatures
- Missing DMARC policy
- Reply-To address mismatch
- Sender spoofing
- Suspicious sender IP addresses
- Emotional manipulation
- Financial scam content
- Urgency tactics

## Outcome
- The analysis successfully distinguished legitimate emails from phishing emails using email header analysis and authentication mechanisms. The project demonstrates practical skills in email forensics, phishing detection, and cybersecurity analysis.

## Skills Demonstrated

- Email Header Analysis
- Email Authentication (SPF, DKIM, DMARC)
- Email Forensics
- Phishing Detection
- Threat Analysis
- Cybersecurity Documentation
## Author
Devisha Bhatia Cyber Security Intern - Future Interns
