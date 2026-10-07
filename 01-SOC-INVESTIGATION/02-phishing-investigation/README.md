# Project 02 - Phishing Investigation

## Summary
One or two plain-English sentences: what the email was and your verdict.

## Email details
 Sender (display name and address): "Microsoft Account Team" <support@micros0ft-security-alerts.com>
- Subject: URGENT: Your account will be closed in 24 hours
- Date:6 october 2026
- Sample source: (Made -up practise email(not a real message))

## Red flags found
1.Lookalike sender domain: "micros0ft" uses a zero instead of the letter "o", and the display name pretends to be Microsoft.
2. Urgent, threatening language: "account will be closed in 24 hours" is designed to make the reader panic and act without thinking.
3. Generic greeting: "Dear Customer" instead of my name suggests a mass-mailed message.
4. Suspicious link: the login link goes to an unrelated .xyz domain, not microsoft.com.
5. Credential request: the email asks me to verify my password, which a genuine company would never do by email.

## Header analysis
| Check | Result | Meaning |
|---|---|---|
| SPF | | |
| DKIM | | |
| DMARC | | |

## Indicators of compromise
- URLs:
- Sender IP:
- Attachment names or hashes:

## Tool results
VirusTotal, URLScan.io and AbuseIPDB findings, with screenshots.

## Verdict
Phishing / Suspicious / Legitimate, and why.

