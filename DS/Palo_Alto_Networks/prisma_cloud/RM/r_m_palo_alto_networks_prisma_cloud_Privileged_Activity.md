Rules by Product and UseCase
============================
Vendor: Palo Alto Networks
--------------------------
### Product: [Prisma Cloud](../ds_palo_alto_networks_prisma_cloud.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   0    |         4          |       4        |    4    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| failed-logon         | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |        |
| security-alert       | <b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |        |
| web-activity-allowed | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity |        |
| web-activity-denied  | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity |        |