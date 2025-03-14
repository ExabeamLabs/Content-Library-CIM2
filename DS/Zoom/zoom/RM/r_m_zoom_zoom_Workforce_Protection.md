Rules by Product and UseCase
============================
Vendor: Zoom
------------
### Product: [Zoom](../ds_zoom_zoom.md)
### Use-Case: [Workforce Protection](../../../../UseCases/uc_workforce_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  11   |   5    |         5          |       4        |    4    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| web-meeting-started    | <b>T1078 - Valid Accounts</b><br> ↳ <b>WCA-MTOW-A</b>: Abnormal web conference meeting time<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>WCA-MTOW-A</b>: Abnormal web conference meeting time    |  • <b>WCA-MTOW</b>: Web conference meeting start time for user    |
| web-meeting-updated    | <b>T1078 - Valid Accounts</b><br> ↳ <b>WCA-DP</b>: Meeting updated to remove password<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>WCA-DP</b>: Meeting updated to remove password    |    |
| webconference-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>WCA-Ucountry-A</b>: Abnormal web conference login country for user<br> ↳ <b>WCA-TOW-A</b>: Abnormal web conference login time<br> ↳ <b>WCA-Tor-IP</b>: User performs web conference login from a known Tor exit node<br> ↳ <b>WCA-Threat-IP</b>: User performs web conference login from a known malicious IP<br> ↳ <b>WCA-Ransomware-IP</b>: User performs web conference login from an IP associated with Ransomware<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>WCA-Ucountry-A</b>: Abnormal web conference login country for user<br> ↳ <b>WCA-TOW-A</b>: Abnormal web conference login time<br> ↳ <b>WCA-Tor-IP</b>: User performs web conference login from a known Tor exit node<br> ↳ <b>WCA-Threat-IP</b>: User performs web conference login from a known malicious IP<br> ↳ <b>WCA-Ransomware-IP</b>: User performs web conference login from an IP associated with Ransomware<br><br><b>T1090 - Proxy</b><br> ↳ <b>WCA-Tor-IP</b>: User performs web conference login from a known Tor exit node<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>WCA-Tor-IP</b>: User performs web conference login from a known Tor exit node |  • <b>WCA-TOW</b>: Web conference login time for user<br> • <b>WCA-Ucountry</b>: Web conference login countries for user    |
| webconference-operations-activity | <b>T1098 - Account Manipulation</b><br> ↳ <b>WCA-OU-F</b>: First time user performs web conference administrative activity<br> ↳ <b>WCA-OU-A</b>: Abnormal web conference administrative activity by user<br> ↳ <b>WCA-OA-F</b>: First time for any user in the organization to perform this web conference administrative activity<br> ↳ <b>WCA-OA-A</b>: Abnormal for any user in the organization to perform this web conference administrative activity    |  • <b>WCA-OA</b>: Web conference admin activities in the organization<br> • <b>WCA-OU</b>: Web conference admin users in the organization |