# Lab 6 --- Basic Firewall Configuration

## Task 1 --- Install the Firewall

Run:

    sudo apt install ufw

### Screenshot

(!<img width="1476" height="2048" alt="image" src="https://github.com/user-attachments/assets/6d891215-6986-4eef-a3fa-1f8730f4477f" />
)

------------------------------------------------------------------------

## Task 2 --- Enable the Firewall

Run:

    sudo ufw enable

### Screenshot

(!<img width="1690" height="2048" alt="image" src="https://github.com/user-attachments/assets/83997f05-c4fd-4d0b-beb7-e45f35d0dcb1" />
)

### Questions

1.  What message appears after enabling the firewall?
  When the firewall is enabled, a message appears confirming that UFW (Uncomplicated Firewall) is active and enabled on system startup. It may also warn that existing SSH connections could be disrupted if SSH is not allowed first.
3.  Why are firewalls important?
 Firewalls are important because they act as a security barrier between a device/network and potential threats. They monitor and control incoming and outgoing traffic based on predefined rules, helping to block unauthorized access, malware, and suspicious network activity.

------------------------------------------------------------------------

## Task 3 --- Allow SSH Access

Run:

    sudo ufw allow ssh
    sudo ufw status

### Screenshot

(!<img width="1726" height="2048" alt="image" src="https://github.com/user-attachments/assets/2a05ea58-fce5-4e3f-9c68-6c542e07e8de" />
)

### Questions

1.  What rule was added?
  The rule added was to allow incoming SSH connections (port 22) using UFW. This permits remote access to the system through SSH.
3.  Why must SSH be allowed?
SSH must be allowed so that administrators can remotely access and manage the system securely. Without this rule, enabling the firewall could block SSH and prevent remote login.
### Reflection

Explain how firewalls help protect systems from unauthorised access.
Firewalls help protect systems by controlling which network connections are allowed or blocked. They prevent unauthorized users from accessing the system and reduce the risk of attacks such as scanning, intrusion attempts, and malware communication. By setting rules like allowing SSH and blocking unwanted traffic, firewalls ensure that only trusted connections are permitted. This improves the overall security of the system and reduces exposure to cyber threats.
