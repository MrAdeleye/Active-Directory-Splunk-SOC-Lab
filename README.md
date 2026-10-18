 <h1> Active-Directory-Splunk-SOC-Lab  </h1>
Teaching Windows to talk. Teaching Splunk to listen. Learning what happens when things go wrong


<h2>Description</h2>
This project is a hands-on security monitoring lab built with VirtualBox, Windows Server, Windows, Sysmon, Splunk, and an increasingly suspicious number of troubleshooting sessions.

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

-<b>Installed Sysmon on the Windows endpoint.
-<b>Verified that the Microsoft-Windows-Sysmon/Operational event channel exists and contains events.
-<b>Installed the Splunk Universal Forwarder on both my windows server and windows 10 
-<b>Configured Windows Application, Security, System, and Sysmon event log collection.
-<b>Created the endpoint index in Splunk for endpoint data.

Splunk Integration and Troubleshooting

