# MDATP_Egregor_Ransomware
Below is a custom made Query which you can run in your Microsoft Defender - Advanced Hunting to look for activity related to Egregor Ransomware.
It's looking for any outbound communication from your Organization's Endpoints towards well known IPs/URLs that are associated with the Egregor Ransomware,for the last 7 days.
You can adjust the Timestamp to search for a longer period of time ( e.g ago(15d) , ago(30d) etc).
The IPs/Urls in the query are based on Cyber Threat Intelligence reports that are published so far ( MAR-2021).In case you come up to additional IOCs feel free to add them into the query.

Microsoft Defender - Advanced Hunting
Advanced hunting is a query-based threat-hunting tool that lets you explore up to 30 days of raw data. You can proactively inspect events in your network to locate threat indicators and entities. The flexible access to data enables unconstrained hunting for both known and potential threats. Advanced hunting is based on Kusto query language.
