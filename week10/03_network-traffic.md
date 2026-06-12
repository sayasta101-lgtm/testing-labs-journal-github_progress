# Lab 5 --- Observing Network Traffic on Rapsberry Pi

## Task 1 --- Install tcpdump

Run:

    sudo apt install tcpdump

### Screenshot


(!<img width="1476" height="2048" alt="image" src="https://github.com/user-attachments/assets/1f3b7fc9-eb5a-4b63-865c-a9169d562ce7" />
)

------------------------------------------------------------------------

## Task 2 --- Capture Network Traffic

Run:

    sudo tcpdump

Let the capture run for about 20 seconds.

### Screenshot

(!<img width="1690" height="2048" alt="image" src="https://github.com/user-attachments/assets/17a0dd61-7f7b-4e25-8665-92b083f0e156" />
)

### Questions

1.  What types of traffic do you observe? You can observe different types of network traffic such as TCP packets, UDP packets, ARP requests, and ICMP messages. These represent communication between devices, network discovery, and data transmission.
2.  Can you identify IP addresses? Yes, tcpdump shows both source and destination IP addresses for each packet. This helps identify which devices are communicating on the network.
3.  Do you see DNS queries? Yes, DNS queries may appear when a device tries to resolve domain names into IP addresses. These are usually UDP packets sent to port 53.

### Reflection

Explain what network monitoring can reveal about system activity.
Network monitoring reveals real-time system activity, including which devices are communicating, what services are being accessed, and how frequently data is being sent. It helps in diagnosing network issues, detecting unusual behaviour, and understanding how applications use the network.

------------------------------------------------------------------------

## Task 3 --- Security Discussion

### Questions

1.  Could sensitive information appear in network traffic? Yes, if communication is not encrypted, sensitive data such as usernames, passwords, and personal information can be exposed in network traffic.
2.  Why is HTTPS important for protecting communications? HTTPS encrypts data between the user and the server, preventing attackers from reading or modifying the information while it is being transmitted. It ensures confidentiality and integrity of data.

### Reflection

Describe what you learned about network visibility and security.
This activity showed that network traffic is highly visible and can reveal a lot of system activity. Without encryption, sensitive information can be exposed and intercepted. I learned that tools like tcpdump are useful for monitoring and troubleshooting networks, but also highlight the importance of using secure protocols like HTTPS to protect data.
