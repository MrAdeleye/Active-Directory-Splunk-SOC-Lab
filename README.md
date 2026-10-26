 <h1> Active-Directory-Splunk-SOC-Lab  </h1>
Teaching Windows to talk. Teaching Splunk to listen. Learning what happens when things go wrong


<h2>Description</h2>
This project is a hands-on security monitoring lab built with VirtualBox, Windows Server, Windows, Sysmon, Splunk, and a suspicious number of troubleshooting sessions.

The goal is to build a small enterprise-style environment, collect endpoint telemetry, centralize logs in Splunk, and eventually use that data to investigate suspicious activity.

Not just installing security tools and admiring the dashboards. I want to understand what the logs are telling me, how to investigate them, and how to turn findings into useful detections.



<br />

<h2> Environments & Tools used </h2>


Windows Server 2022 Active - Directory server and  domain controller

Windows 10 - Endpoint for domain and security monitoring experiments

Ubuntu Server - Hosts Splunk Enterprise for centralized log collection and analysis

Sysmon - Collects detailed Windows system activity

Splunk Universal Forwarder - Forwards Windows event data to Splunk

VirtualBox 7.2 - Runs the virtual lab environment

Kali Linux - Supporting security testing and lab ex


<h2> Current Progress </h2>
 Active Directory Setup

- <b>Installed Active Directory Domain Services on Windows Server 2022
- <b>Promoted the server to a domain controller.
- <b>Configured the Windows 10 client's DNS settings to use the domain controller..
- <b>Successfully joined the Windows 10 client to the Active Directory domain.
- <b>Created an administrative user for lab administration.
  

Endpoint Monitoring

- <b>Installed Sysmon on the Windows endpoint.
- <b>Verified that the Microsoft-Windows-Sysmon/Operational event channel exists and contains events.
- <b>Installed the Splunk Universal Forwarder on both my windows server and windows 10 
- <b>Configured Windows Application, Security, System, and Sysmon event log collection.
- <b>Created the endpoint index in Splunk for endpoint data.

Splunk Integration and Troubleshooting
- <b>Configured Splunk Enterprise on Ubuntu Server to receive forwarded data on TCP port 9997.
- <b>Configured the Universal Forwarder to send events to the Splunk server at 192.168.10.5:9997.
- <b>Tested network connectivity between the Windows endpoint and the Splunk receiver.
- <b>Troubleshot a forwarding destination mismatch that caused the forwarder to attempt connections to an incorrect IP address.
- <b>Corrected the destination and confirmed that Windows endpoint events are now appearing in Splunk.

This troubleshooting process reinforced the importance of validating effective configuration, checking service status, testing network connectivity, and reviewing forwarder logs when diagnosing ingestion problems.

<h2> Next Phase: Simulating a Business Network </h2>

The next stage is to populate Active Directory with fictional employee accounts and organize them into a realistic business structure.

Planned tasks:

- <b>Use PowerShell to create multiple test users.
- <b>Organize users into Organizational Units (OUs).
- <b>Create department-based and role-based security groups.
- <b>Assign group memberships according to job responsibilities.
- <b>Test authentication and access permissions from the domain-joined Windows 10 client.
- <b>Practise account provisioning, role changes, and account deactivation.

All accounts and identities will be fictional and restricted to the lab environment.

Planned SOC Investigations

Once the domain environment and logging pipeline are validated, I plan to generate and investigate security-relevant activity, including:
Successful and failed Windows logons.
Repeated authentication failures and account lockouts.
New user and computer account creation.
Security group membership changes.
Privileged group modifications.
Suspicious PowerShell activity.
Sysmon process creation and other relevant endpoint events.

Splunk searches will be developed to identify these events, establish useful context, and distinguish expected administrative activity from potentially suspicious behavior.

Planned IAM Exercises

The Active Directory environment will also support a separate focus on Identity and Access Management.

Planned exercises include:
Identity lifecycle management: onboarding, role changes, and offboarding.
Role-based access control: assigning permissions through security groups.
Least privilege: checking whether users have more access than their roles require.
Access reviews: auditing group memberships and privileged accounts.
Account auditing: identifying disabled accounts, stale accounts, and inappropriate access.
PowerShell automation: creating repeatable user administration and reporting scripts.

These exercises are intended to demonstrate practical identity administration and access governance concepts using on-premises Active Directory.

<h2>Project walk-through:</h2>

<p align="center">
Conceptual Diagram of Active Directory Lab + Soc Project   <br/>
<img src="https://i.imgur.com/ihHtnSc.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
Lab Architechture and Virtual Machines   <br/>
<img src="https://i.imgur.com/tWkiiYH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<p align="center">
Installed & Configured splunk on Ubuntu    <br/>
<img src="https://i.imgur.com/lFjRgep.pngheight" ="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/tOOqUcb.png" ="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

