## SOC Incident Report

Incident Type: SSH Brute Force Attack

Detection Tool: Wazuh SIEM

Severity Level: Medium

Description:
Multiple failed SSH login attempts were detected on the Ubuntu server.
The attack originated from the Kali Linux machine and attempted to gain
unauthorized access using invalid credentials.

Detection Method:
Wazuh monitored the Linux authentication logs and triggered alerts
for repeated authentication failures.

Source IP Address:
192.168.56.

Target System:
Ubuntu Linux Server

Log Source:
/var/log/auth.log

Indicators of Compromise:
- Multiple failed SSH authentication attempts
- Repeated login attempts within a short time period

MITRE ATT&CK Technique:
T1110 – Brute Force

Response Actions:
1 Identify attacker IP address
2 Block IP using firewall
3 Monitor additional login attempts
4 Investigate potential credential compromise

Conclusion:
The attack simulation successfully demonstrated Wazuh's ability to detect
SSH brute force attempts by monitoring Linux authentication logs.
