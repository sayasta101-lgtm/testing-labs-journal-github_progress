# Exploring Your System's Security

## Task 1 --- List System Users

Run:

    cat /etc/passwd

### Screenshot

(!<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/7b6bb41a-7aaa-4e8a-9aba-9754706ba194" />
)

### Questions

1.  How many users exist on the system?
2.  Which accounts appear to be system accounts?
   System accounts usually:

Have UID below 1000 (Linux standard)
Examples:
root
daemon
bin
sys
www-data
systemd-*
4.  Why do operating systems create system accounts?
System accounts are created to:

Run background services (like networking, web servers)
Improve security by separating services from real users
Prevent applications from needing full admin access
Reduce damage if a service is compromised

### Reflection

Explain why understanding system users is important for cybersecurity.

Understanding system users is important for cybersecurity because user accounts control who has access to a system and what they are allowed to do. If you don’t understand how system users are structured, it becomes difficult to detect security risks or unauthorized access.

System users include both real people and special service accounts used by the operating system. Cybersecurity professionals need to know the difference because system accounts (like background services) are normally trusted, while regular user accounts represent real individuals. If an attacker creates a fake account or compromises an existing one, it can be used to access sensitive data or escalate privileges.

It is also important for identifying unauthorised or suspicious accounts. For example, unknown usernames or accounts with high privileges could indicate a breach or malware presence. Additionally, understanding user permissions helps ensure that users only have the access they need, which follows the principle of least privilege and reduces potential damage from attacks.

Overall, knowing system users helps protect confidentiality, integrity, and availability of the system by ensuring only the right people and services have the right level of access.

## Task 2 --- Inspect Running Processes

Run:

    ps aux

### Screenshot

(!<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/85bf0ccb-c323-459c-9ffe-a17089a1b5c6" />
)

### Questions

1.  Which processes are running as `root`?
2.  Why can processes running as root be dangerous?
3.  What could happen if a malicious program ran with root privileges?

### Reflection

What did you learn about system processes and security?

System processes are the programs and services that run in the background of an operating system to keep it functioning, such as managing files, networks, and hardware. From a security perspective, I learned that these processes are very important because they often run with different privilege levels, including powerful ones like root.

One key insight is that processes running as root have full control over the system. This means they can access, modify, or delete any file and change system settings. While this is necessary for essential services, it also makes them a major security risk if they are misused or compromised.

I also learned that not all processes are user-initiated; many are automatically started by the system. Because of this, it is important to regularly monitor running processes using tools like ps aux to identify anything unusual or suspicious. Malware often hides as normal-looking processes, so understanding what “normal” looks like helps detect threats early.

Overall, system processes are critical for functionality, but they must be carefully monitored because any vulnerable or malicious process running with high privileges can seriously compromise the entire system.

## Task 3 --- Identify Open Network Ports

Run:

    ss -tuln

### Screenshot

(!<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/30bc0497-22c8-4c6f-9362-681a18ea063b" />
)

### Questions

1.  Which ports are open?
2.  Which services appear to be listening?
3.  Why might open ports represent a security risk?

### Reflection

Explain the relationship between open ports and potential attack
surfaces.
Open ports are directly linked to a system’s attack surface, which refers to all possible entry points an attacker can use to access or exploit a system.

When a port is open, it means a service is actively listening for incoming network connections (for example SSH on port 22 or a web server on port 80/443). Each open port therefore acts as a doorway into the system.

The more open ports a system has, the larger its attack surface becomes. This increases the number of ways an attacker might:

Scan for vulnerable services
Exploit misconfigured software
Brute-force login services (e.g., SSH)
Send malicious requests to exposed applications

Even if a service is legitimate, it can still become a security risk if:

It is outdated and has known vulnerabilities
It is misconfigured
It has weak authentication
It is unnecessary but still running

For example:

An open SSH port (22) can be targeted for password attacks
An exposed web server (80/443) can be attacked through web vulnerabilities like SQL injection or XSS
