# 30-Day-Challenge-SOC-Analyst-Projects

## DAY 1
Created a logical diagram.

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/8e4b299a-cd1d-49bd-8c75-21a92d9ba5c4" />

## DAY 2

E-ELK | Elasticsearch
- Search and engine database platform
  
L-ELK | Logstash
- Collects logs and data

K-ELK | Kibana
- Data Visualization and management tool
- Beats/Agents

-- In summary, ELK is great for centralized logging, flexibility, visualizations, and scalability. 

## DAY 3
- Installed VULTR and updated the repositories.
- Downloaded and installed Elasticsearch via the terminal, then added the VPN IP address and port to the elasticsearch.yml file.
- Configured the VULTR firewall to allow access only from the specified IP address.
- Started Elasticsearch using systemctl enable elasticsearch.service.

## DAY 4
- Installed Kibana on the system.
- Configured the IP address and port using nano.
- The Elastic web interface is now accessible after enabling port 5601.
- Retrieved the tokens from Elasticsearch and used them on the private network to access Elasticsearch via its private IP address.

## DAY 5
- Windows server installation have been completed.

## DAY 6
- Elastic Agent: A single agent that manages collected data.
- Managed by Fleet: The Elastic Agent’s lifecycle, policies, and configuration are centrally managed through Fleet.
    - Standalone mode: All configuration is applied to the Elastic Agent manually.
- Beats: Lightweight data shippers used to send data from different sources to Elasticsearch.
- Fleet Server: The component that connects Elastic Agents to Fleet, making it easy to apply changes, updates, and policy adjustments.

## DAY 7
- Installed Elastic Agent on Windows server.
- Enrolled the Windows server into a Fleet.

## DAY 8
- Sysmon (System Monitor): A tool that helps monitor system events in detail. 
- A free Microsoft tool that is part of the Sysinternals Suite.
- Monitors a wide range of system events.
- Process GUID: Correlates events across the system, making it easier to see the bigger picture.

- Event ID 1 – Process Creation:
    - Tracks process creation in detail, including file hashes.
- Event ID 3 – Network Connection:
    - Logs TCP/UDP connections (UDP is disabled by default) and includes source and destination IP addresses, hostnames, port numbers, and IPv6 status.
- Event ID 6 / 7 / 8 – Driver Image Load & Create Remote Thread:
    - Helps identify potential defense-evasion techniques commonly monitored by EDR (Endpoint Detection and Response) solutions.
- Event ID 10 – Process Access: 
    - Detects attempts by hacking tools to read the memory of sensitive processes, such as the Local Security Authority (LSASS.exe), to steal credentials.
- Event ID 22 – DNS Query: 
    - Generated when a process performs a DNS query.
 
## DAY 9
- Installed and configured Sysmon on the Windows server machine.
- Confirmed it started to generate events.
  
<img width="662" height="154" alt="image" src="https://github.com/user-attachments/assets/87353322-4d1e-4484-86a9-7f735244e0b0" />

## DAY 10
- Confirmed that Sysmon is integrated into Elasticsearch.
- Sysmon and Microsoft Defender logs are successfully ingested into Elasticsearch.
<img width="368" height="28" alt="image" src="https://github.com/user-attachments/assets/78099a29-010b-4c37-b5da-70d3a520366f" />

## DAY 11
- Brute Force Attack: Trying every combination to find the correct password.
- Dictionary Attack: Using common words or phrases to guess the correct password.
- Credential Stuffing: Using credential information to find the password, such as known or exposed passwords or usernames.

Hydra, HashCat, John the Ripper: Brute Force Attack tools 

## DAY 12
- Set up own SSH server in the cloud.
- Got failed autentication attempts in the server.

## DAY 13
- Installed Elastic agent on the SSH Server
- Confirmed logs are generated.

## DAY 14
- Created alert and dashboard for SSH Brute Force

<img width="2167" height="450" alt="image" src="https://github.com/user-attachments/assets/554eb797-ece0-447a-a5ca-f0d0cbf2b57f" />

## DAY 15
- RDP (Remote Desktop Protocol)
To keep track of services that is exposed to the internet:
- Shodan
    - Port3389 mostly is the protocol for RDP
- Censys

## DAY 16
- Event ID 4625: Documents every failed login attempt on a Windows computer.
- Created alerts and configured for both Windows (RDP) and Ubuntu (SSH) servers.
- Alert dsplays the user.name and source.ip for all failed authentication attempts.

## DAY 17
- Created dashboards for both Windows (RDP) and Ubuntu (SSH) servers tracking for both successful and failed attempts.
- Captured user.name, source.ip, and source.geo.country_name of these attempts. 

<img width="2170" height="412" alt="image" src="https://github.com/user-attachments/assets/2fb1ff35-5c40-4ed8-b243-bf9efabcd499" />
<img width="2171" height="418" alt="image" src="https://github.com/user-attachments/assets/1149e0b2-8913-472a-bcd3-48d0e8a4c698" />
<img width="2190" height="424" alt="Screenshot 2026-02-13 111602" src="https://github.com/user-attachments/assets/74f67017-6290-4769-87e0-14e2c6531b96" />
<img width="2144" height="426" alt="Screenshot 2026-02-13 111746" src="https://github.com/user-attachments/assets/c635335d-55a1-4429-aed2-e0619404b53b" />

## DAY 18
- C2 (Command & Control)
  - Metasploit: A widely used penetration testing tool for developing and executing exploit code against a remote target.
  - Fortra: The industry-standard adversary simulation tool used by both red teams and real-world threat actors.
  - The DFIR Report: A highly respected security resource that provides detailed case studies and technical breakdowns of real-world intrusions and malware campaigns.
  - Sliver: A cross-platform, open-source C2 framework designed for red teaming and adversary simulation.
  - Mythic: A collaborative, cross-platform C2 framework specifically designed to support complex red team operations and pluggable communication profiles.
 

## DAY 19


