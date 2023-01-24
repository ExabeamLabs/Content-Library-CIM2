Rules by Product and UseCase
============================
Vendor: GoAnywhere
------------------
### Product: [GoAnywhere MFT](../ds_goanywhere_goanywhere_mft.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       7        |    7    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| failed-logon  | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive |        |
| file-delete   | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |        |
| file-download | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |        |
| file-upload   | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |        |