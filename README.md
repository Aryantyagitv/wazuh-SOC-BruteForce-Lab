# wazuh-SOC-BruteForce-Lab
SOC monitoring lab detecting SSH brute force attacks using Wazuh SIEM
# SOC Brute Force Detection Lab using Wazuh

## Overview

This project demonstrates a basic Security Operations Center (SOC) monitoring lab using Wazuh SIEM. A brute force SSH attack was simulated from Kali Linux against an Ubuntu server. Wazuh monitored authentication logs and generated security alerts.

## Lab Environment

Attacker Machine: Kali Linux
Target Server: Ubuntu Linux
SIEM Platform: Wazuh
Virtualization: VirtualBox

## Attack Simulation

A brute force attack was simulated by repeatedly attempting to log into the Ubuntu server using invalid SSH credentials.

Example command:

ssh fakeuser@192.168.56.103

Multiple failed attempts were generated to trigger authentication failure logs.

## Log Analysis

Authentication logs were monitored on the Ubuntu server.

Command used:

sudo tail -f /var/log/auth.log

These logs recorded failed login attempts.

## Wazuh Detection

Wazuh detected the brute force activity by analyzing the authentication logs and generating alerts.

Example alerts:

SSH authentication failure
Password guessing attempt

## MITRE ATT&CK Mapping

Technique:

T1110 – Brute Force

## Incident Response

If this attack occurred in a production environment, a SOC analyst would:

1 Identify the attacker IP address
2 Block the IP using firewall
3 Monitor further login attempts
4 Investigate possible credential compromise
