# Project 01 – SOC Investigation

## Summary
A practice alert showed repeated failed logins followed by a success, then a suspicious file. I investigated and concluded this was a likely brute-force attack with the account compromised. This is a made-up practice scenario.

## Log evidence
```
09:01:12 FAILED login user=admin from 203.0.113.45
09:01:15 FAILED login user=admin from 203.0.113.45
09:01:18 FAILED login user=admin from 203.0.113.45
09:01:21 FAILED login user=admin from 203.0.113.45
09:01:24 FAILED login user=admin from 203.0.113.45
09:01:27 SUCCESS login user=admin from 203.0.113.45
09:03:40 New file created: C:\Temp\update.exe
```

## Timeline
| Time | Event |
|---|---|
| 09:01:12–09:01:24 | Five failed logins for admin from one IP |
| 09:01:27 | Successful login from the same IP |
| 09:03:40 | update.exe created in C:\Temp |

## Indicators of compromise
- IP address: 203.0.113.45
- File: C:\Temp\update.exe
- Account: admin

## MITRE ATT&CK mapping
| Tactic | Technique | Evidence |
|---|---|---|
| Credential Access | Brute Force (T1110) | Five rapid failed logins |
| Initial Access | Valid Accounts (T1078) | Successful login after failures |

## Severity
High. The attacker logged in and a suspicious executable appeared within minutes.

## Recommended actions
1. Disable or reset the admin account password.
2. Block 203.0.113.45 at the firewall.
3. Isolate the host and scan update.exe.
4. Check for other logins from the same IP.
5. Enable account lockout and multi-factor authentication.

## What I learned
(I learned how to spot a brute-force attack in login logs: many failed attempts from one IP address in a short time. A successful login straight after those failures is a serious warning sign, because it suggests the attacker guessed the password. I also learned to look at what happened next, such as the suspicious file update.exe appearing in C:\Temp, since that can show the attacker is trying to install malware. I mapped the activity to MITRE ATT&CK techniques (Brute Force and Valid Accounts) and practised writing clear recommended actions: reset the account, block the IP, isolate the host and enable account lockout and multi-factor authentication. This was a made-up practice scenario, so my next step is to repeat the process with real log data in a lab such as Splunk or Security Onion)

