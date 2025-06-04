# Detection Lab

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps

*Ref 1: Network Diagram*

![AD Topology](https://github.com/user-attachments/assets/61fc064b-2f71-48b6-b2d1-2c3b29548361)

*Ref 2: Configuring Splunk Server Static IP*

![Splunk Server IP Config](https://github.com/user-attachments/assets/86f24108-125f-4d2e-a9b0-c32fa5e3db22)

I ran into an issue here where the cloud init wanted to keep reverting back to the dhcp settings after reboot.  I used the command [sudo touch /etc/cloud/cloud-init.disabled] to tell it to stop making changes, then renamed it and made a new configuration file with the [sudo nano /etc/netplan/01-static-ip.yaml] command. 

*Ref 3: Configuring Splunk Server Static IP with new netplan file*

![Splunk Server IP Config new](https://github.com/user-attachments/assets/c8055cca-4a64-46c5-80d3-b9ea023d2aa8)

After doing that and rebooting, I was able to confirm connection to the splunk server from the Windows 10 machine

*Ref 4: Confirming connection to splunk server from Windows machine via web browser*

![Confirming Splunk login after IP configuration](https://github.com/user-attachments/assets/7cf43502-0e5e-437a-8339-52055855425e)

*Ref 5: Configuring Splunk Forwarder and Sysmon on Target PC*

![Configuring Sysmon and Splunk Forwarder](https://github.com/user-attachments/assets/5b9ac211-524b-45b7-a91a-ac8e2bc2421b)

*Ref 6: Confirming Splunk server is receiving traffic from Target PC into newly created endpoint index*

![Confirming Splunk Forwarding to Server](https://github.com/user-attachments/assets/30b16b20-9f62-408d-8a08-9f8986aab8cf)

*Ref 7: Confirming Splunk server is receiving traffic from Target PC AND ADDC into newly created endpoint index*

![Confirming Splunk Forwarding to Server 2](https://github.com/user-attachments/assets/2e83d15c-f745-468e-9821-a841c7807f17)
