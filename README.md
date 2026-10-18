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
 Windows telemetry collection

- <b>Installed and configured Sysmon on the Windows systems.
- <b>Installed and configured Splunk Universal Forwarder.
- <b>Configured Windows event log inputs, including Application, Security, System, and Sysmon Operational logs.
- <b>Configured forwarding to the Splunk receiver over TCP port 9997..
- <b>Created the endpoint index in Splunk.
- <b>Verified that endpoint data is arriving in the Splunk interface

 Troubleshooting the pipeline

-<b>Getting logs from Windows into Splunk involved more than installing the software.

-<b>I worked through forwarding configuration issues, network connectivity checks, receiver port configuration, and Windows event channel verification.One incorrect port number was enough to waste time. A useful reminder that sometimes the problem is not advanced cybersecurity. Sometimes it is one extra digit.
This troubleshooting is part of the project, not something to hide. The aim is to document the symptoms, investigation, fix, and verification for each issue.


