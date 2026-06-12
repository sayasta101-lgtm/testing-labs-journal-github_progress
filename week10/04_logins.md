# Detecting Suspicious Activity

## Objective

Learn about **detective security controls**.

---

## Step 1 – View authentication logs

```bash
sudo cat /var/log/auth.log
```

## Step 2 – Search for login attempts
```bash
grep "Failed password" /var/log/auth.log
```

## Step 3 – View recent logins
```bash
last
```

## Questions
- What information appears in authentication logs? Authentication logs show system login activity such as successful and failed login attempts, usernames used, timestamps, IP addresses of login attempts, and authentication methods (e.g., password or SSH). They help track who accessed the system and when.
- Why are logs important in cybersecurity? Logs are important because they provide a record of system activity. They help detect security incidents, investigate breaches, monitor user behaviour, and identify system errors. Without logs, it would be difficult to trace attacks or unauthorized access.
- What might indicate suspicious activity? Suspicious activity may include multiple failed login attempts, repeated logins from unknown IP addresses, login attempts at unusual times, or access using unfamiliar usernames. These patterns can indicate brute-force attacks or unauthorized access attempts.


## Deliverables
Include screenshots of:
- authentication logs
- failed login search results
