Splunk Learning Notes
📌 Overview
These notes summarize what I learned during the Splunk VPN Monitoring Lab.
The goal was to understand how Splunk ingests, parses, indexes, and searches machine‑generated data.

🧠 Key Concepts Learned
1. Splunk Architecture
Forwarder → Sends data to Splunk

Indexer → Stores and processes data

Search Head → Allows users to run SPL queries

Understanding this flow helped me see how logs move through a SIEM.

2. Adding Data to Splunk
Steps I performed:

Upload file → VPNlogs.json

Set Source Type → _json

Configure Host → VPN_Connections

Select Index → VPN_Logs

Review & Submit

This taught me how Splunk interprets structured data.

3. Understanding Fields
Splunk automatically extracted fields such as:

UserName

Source_ip

Source_Country

EventTime

action

protocol

port

These fields were essential for filtering and analysis.

4. SPL (Search Processing Language)
I learned how to:

Filter events

Search by username

Search by IP

Exclude countries

Count events

Extract values

Example:

spl
index="VPN_Logs" UserName="Maleena"
5. SOC‑Style Investigation
I practiced:

Identifying suspicious IPs

Tracking user activity

Filtering out noise

Understanding event timelines

Correlating fields
