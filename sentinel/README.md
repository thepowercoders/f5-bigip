# Sentinel Workbooks
## Introduction
This directory holds some workbooks which I have built for Azure Sentinel. There are 2 workbooks which are provided in the Content Hub ( F5 BIG-IP ASM and F5 BIG-IP System Metrics) which provide ASM (WAF) info and system performance stats. However, there are no workbooks for AFM for either the firewall or the Protection Inspection (IDPS) features. I've therefore created two workbooks to provide this information.

I've also created some other workbooks which you may find useful and provides the following:
* replicates information from the BIG-IP GUI for key screens like Local Traffic / Virtual Servers and Local Traffic / Pools
* checks for certificate expiry of traffic certificates

## F5 BIG-IP Intrusion Detection/Prevention (IDPS) Insights
[This workbook](F5_BIG-IP_IDPS.workbook?plain=1) has been written to match the ASM workbook provided by F5 in the Content Hub but specifically for the Protocol Inspection (IDS/IPS) feature. It provides the same graphics and information as ASM as follows:
* Summary of all AFM events for each device
* All IDPS Events received in the time period grouped by Action (allow, drop or reject) and including:
   * the inspection vector name
   * the risk assigned to the vector by F5
   * total count of each vector which has been triggered
* IDPS violations over time
* A summary table and pie-chart of all intrusion attempts
* A table summarising the attacks with client IP, F5 device, Service and Protocol Inspection profile

