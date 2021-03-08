# MD_Egregor
Below is a custom made Query which you can run in your Microsoft Defender - Advanced Hunting to look for activity related to Egregor Ransomware.
It's looking for any outbound communication from your Organization's Endpoints towards well known IPs/URLs that are associated with the Egregor Ransomware,for the last 7 days

DeviceNetworkEvents
| where Timestamp > ago(7d)
| where RemoteIP == "49.12.104.241"
	or RemoteIP == "185.238.0.233"
	or RemoteIP == "45.153.242.129"
	or RemoteIP == "45.11.19.70"
	or RemoteIP == "217.8.117.148"
	or RemoteIP == "80.226.253.106"
	or RemoteIP == "185.246.130.118"
	or RemoteIP == "139.60.161.62"
	or RemoteIP == "37.1.210.119"
	or RemoteUrl == "boobong.net"
| project DeviceName, DeviceId, LocalPort, LocalIP, RemotePort, RemoteIP, InitiatingProcessFileName

You can adjust the Timestamp to search for a longer period of time ( e.g ago(15d) , ago(30d) etc)
The IPs/Urls in the query are based on Cyber Threat Intelligence reports that are published so far ( MAR-2021).In case you come up to additional IOCs feel free to add them into the query.

Microsoft Defender - Advanced Hunting
Advanced hunting is a query-based threat-hunting tool that lets you explore up to 30 days of raw data. You can proactively inspect events in your network to locate threat indicators and entities. The flexible access to data enables unconstrained hunting for both known and potential threats. Advanced hunting is based on Kusto query language.
