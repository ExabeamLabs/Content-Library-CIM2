Rules by Product and UseCase
============================
Vendor: McAfee
--------------
### Product: [McAfee Web Gateway](../ds_mcafee_mcafee_web_gateway.md)
### Use-Case: [Workforce Protection](../../../../UseCases/uc_workforce_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   2    |         2          |       1        |    9    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| web-activity-allowed | <b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-OU-JS-F</b>: First job search activity for user in the organization<br> ↳ <b>WEB-OU-JS-A</b>: Abnormal job search activity for user in the organization<br> ↳ <b>WEB-OG-JS-F</b>: First job search activity for user in the peer group<br> ↳ <b>WEB-OG-JS-A</b>: Abnormal job search activity for user in the peer group<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-OU-JS-F</b>: First job search activity for user in the organization<br> ↳ <b>WEB-OU-JS-A</b>: Abnormal job search activity for user in the organization<br> ↳ <b>WEB-OG-JS-F</b>: First job search activity for user in the peer group<br> ↳ <b>WEB-OG-JS-A</b>: Abnormal job search activity for user in the peer group |  • <b>WEB-OG-JS</b>: Job search activities of users in the peer group<br> • <b>WEB-OU-JS</b>: Job search activities of users in the organization |