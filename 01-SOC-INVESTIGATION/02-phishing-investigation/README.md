# Project 02 - Phishing Investigation

## Summary
One or two plain-English sentences: what the email was and your verdict.

## Email details
 Sender (display name and address): "Microsoft Account Team" <support@micros0ft-security-alerts.com>
- Subject: URGENT: Your account will be closed in 24 hours
- Date:6 october 2026
- Sample source: (Made -up practise email(not a real message))

## Red flags found

1. Lookalike sender domain: "micros0ft" uses a zero instead of the letter "o", and the display name pretends to be Microsoft.

2. Urgent, threatening language: "account will be closed in 24 hours" is designed to make the reader panic and act without thinking.

3. Generic greeting: "Dear Customer" instead of my name suggests a mass-mailed message.

4. Suspicious link: the login link goes to an unrelated .xyz domain, not microsoft.com.
   
5. Credential request: the email asks me to verify my password, which a genuine company would never do by email.

## Header analysis
| Check | Result | Meaning |
|---|---|---|
| SPF | Not available (practice email) | A real email would likely fail SPF, because the sender domain is a lookalike. |
| DKIM | Not available (practice email) | Checks the message is signed and unaltered. Would be missing or fail here. |
| DMARC | Not available (practice email) | Tells the receiver what to do with failed emails. Lookalike domains usually have no policy. |

## Indicators of compromise
- URLs:http://account-verify-login.example-secure.xyz/login
- Sender IP: Not available (practice email)
- Attachment names or hashes: None

## Tool results
Won't run, because the email and link are fictional. I would check the URL on VirusTotal and URLScan.io, and the sender IP on AbuseIPDB with a actual email then add screenshots here.

## Verdict
Phishing -the sender use a look alike domain Phishing. 
the message threatens the user with a 24-hour deadline, and  asks for a password through a link to an unrelated domain.
Not what a genuine email will do
