Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - NTLM](../ds_microsoft_event_viewer_-_ntlm.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  11   |   4    |         5          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| ntlm-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>AL-HLocU-F</b>: First local user logon to this asset<br> ↳ <b>AL-HLocU-A</b>: Abnormal local user logon to this asset<br> ↳ <b>AL-UT-F</b>: Logon to New Asset Type<br> ↳ <b>AL-UT-A</b>: Logon to Abnormal asset type<br> ↳ <b>AL-UZ-F</b>: First logon to network zone<br> ↳ <b>AL-UZ-A</b>: Abnormal logon to network zone<br> ↳ <b>AL-GZ-F-new</b>: First logon to network zone for new user of group<br> ↳ <b>AL-GZ-A-new</b>: Abnormal logon to network zone for group of new user<br> ↳ <b>A-AL-DhU-F</b>: First user per asset<br> ↳ <b>A-AL-DhU-A</b>: Abnormal user per asset<br><br><b>T1550 - Use Alternate Authentication Material</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected<br><br><b>T1550.003 - Use Alternate Authentication Material: Pass the Ticket</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected<br><br><b>T1558 - Steal or Forge Kerberos Tickets</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected<br><br><b>T1078.003 - Valid Accounts: Local Accounts</b><br> ↳ <b>AL-HLocU-F</b>: First local user logon to this asset<br> ↳ <b>AL-HLocU-A</b>: Abnormal local user logon to this asset |  • <b>A-AL-DhU</b>: Users per Host<br> • <b>AL-GZ</b>: Network zones accessed by this peer group<br> • <b>AL-UT</b>: Types of hosts<br> • <b>NKL-HU</b>: Users logging into this host remotely |