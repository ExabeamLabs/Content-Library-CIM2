Rules by Product and UseCase
============================
Vendor: F5
----------
### Product: [F5 BIG-IP DNS](../ds_f5_f5_big-ip_dns.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   7    |         2          |       2        |    0    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-failed | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a new country<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which peer group has never had a successful activity    |  • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-OC</b>: Countries for organization<br> • <b>UA-UC</b>: Countries for user activity    |
| web-activity-denied   | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-UT-TOW-A</b>: Abnormal day for this user to access the web via the organization<br> ↳ <b>WEB-UZ-F</b>: First web activity for this user in this zone<br> ↳ <b>WEB-GZ-F</b>: First web activity from this zone for the peer group<br> ↳ <b>WEB-OC-F</b>: First access to an internet IP address in this country for the organization |  • <b>WEB-OC</b>: Web destination countries for org<br> • <b>WEB-GZ</b>: Network zones where users performs web activity in the peer group<br> • <b>WEB-UZ</b>: Network zones where a user performs web activity from<br> • <b>WEB-UT-TOW</b>: Web activity activity time for user |