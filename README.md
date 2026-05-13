# splunk-security-monitoring-lab
📌 Overview
This repository documents my hands‑on work using Splunk Enterprise to ingest, parse, and analyze VPN connection logs.
The goal of the lab was to simulate real SOC analyst tasks such as:

Uploading and indexing log data

Identifying user activity

Investigating suspicious IP addresses

Filtering events by country

Understanding Splunk’s core components (Forwarder, Indexer, Search Head)

This project demonstrates my ability to work with machine‑generated data and perform foundational SIEM analysis.

🧩 Skills Demonstrated
Log ingestion & index creation

SPL (Search Processing Language)

Event filtering & correlation

VPN log analysis

Identifying user activity patterns

Basic threat‑hunting logic

Understanding Splunk architecture

SOC‑style investigation workflow

📁 Dataset
The dataset used in this lab was a JSON‑formatted VPN log file:

Code
VPNlogs.json
It was uploaded into a custom index:

Code
VPN_Logs
🔧 Key SPL Queries
1. Count total events
spl
index="VPN_Logs"
2. Events for user “Maleena”
spl
index="VPN_Logs" UserName="Maleena"
3. Username associated with IP 107.14.182.38
spl
index="VPN_Logs" Source_ip="107.14.182.38"
4. Events from all countries except France
spl
index="VPN_Logs" NOT Source_Country="France"
5. Events associated with IP 107.3.206.58
spl
index="VPN_Logs" Source_ip="107.3.206.58"
📊 Findings
Question	Result
Total events ingested	2862
Events by user “Maleena”	60
Username for IP 107.14.182.38	Smith
Events from all countries except France	2814
Events from IP 107.3.206.58	14
