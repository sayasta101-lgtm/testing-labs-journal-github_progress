# Exploring the CIA Triad

## Objective

Understand the **Confidentiality, Integrity and Availability (CIA)** principles using practical tasks on a Raspberry Pi.

---

# Part 1 – Confidentiality

1. Create a confidential file.

    ```bash
    nano secrets.txt
    ```

1. Write some confidential information.

1. Save the file.

1. Now restrict access:
    ```bash
    chmod 600 secrets.txt
    ```
1. Check permissions:
    ```bash
    ls -l secrets.txt
    ```

**Questions**
- Who can read this file?
- Only the file owner (you) can read and write the file. No other users can access it because the permission is set to 600
- How does file permission protect confidentiality?
- File permissions control who can access data. By using chmod 600, access is restricted so only the owner can read and modify the file, preventing unauthorized users from viewing sensitive information.

## Part 2 – Integrity

1. Create a hash of the file.
    ```bash
    sha256sum secrets.txt
    ```
    _What does "hash" do?
   A hash creates a unique fixed-length value (fingerprint) of the file’s content. It is used to detect any changes in the file.

1. Save the output.

1. Modify the file.
    ```bash
    nano secrets.txt
    ```

1. Run the hash again.


** Questions**
- Did the hash change?
- Yes, the hash changes after modifying the file.
- Why do security systems use hashing?
- Hashing is used to verify data integrity. If even a small change is made to a file, the hash changes completely, helping detect tampering or corruption.


# Part 3 – Availability

1. Check system uptime:
    ```bash
    uptime
    ```

1. List running processes:
    ```bash
    top
    ```

**Questions**
- Why is system uptime important?
- System uptime shows how long a system has been running without interruption. High uptime means the system is reliable and services are consistently available to users.
- What happens if a system is unavailable?
If a system is unavailable, users cannot access services or data. This can lead to downtime, loss of productivity, financial loss, and disruption of services.
## Deliverables
Include:
- Screenshot of file permissions
- !<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/f73f5bb0-610e-45c5-8a26-d19a40194695" />

- Screenshot of hash results
- Answers to questions
- Reflection
    >Explain how this activity demonstrated the CIA triad.
    This activity demonstrated the CIA triad in a practical way. Confidentiality was shown by restricting file access using permissions so only the owner could view the data. Integrity was demonstrated using hashing, where even a small change in the file resulted in a completely different hash value. Availability was shown through system uptime and running processes, highlighting the importance of keeping systems operational for users. Overall, the activity helped me understand how confidentiality, integrity, and availability work together to protect computer systems and data security.
