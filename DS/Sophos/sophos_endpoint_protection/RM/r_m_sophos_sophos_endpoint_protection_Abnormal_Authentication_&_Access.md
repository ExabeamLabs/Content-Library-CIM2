Rules by Product and UseCase
============================
Vendor: Sophos
--------------
### Product: [Sophos Endpoint Protection](../ds_sophos_sophos_endpoint_protection.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   3    |         2          |       1        |    1    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| web-activity-denied | <b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-UT-TOW-A</b>: Abnormal day for this user to access the web via the organization<br> ↳ <b>WEB-UZ-F</b>: First web activity for this user in this zone<br> ↳ <b>WEB-GZ-F</b>: First web activity from this zone for the peer group<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-UT-TOW-A</b>: Abnormal day for this user to access the web via the organization<br> ↳ <b>WEB-UZ-F</b>: First web activity for this user in this zone<br> ↳ <b>WEB-GZ-F</b>: First web activity from this zone for the peer group |  • <b>WEB-GZ</b>: Network zones where users performs web activity in the peer group<br> • <b>WEB-UZ</b>: Network zones where a user performs web activity from<br> • <b>WEB-UT-TOW</b>: Web activity activity time for user |