Rules by Product and UseCase
============================
Vendor: Symantec
----------------
### Product: [Symantec Critical System Protection](../ds_symantec_symantec_critical_system_protection.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   0    |     2      |       4        |    4    |

| Event Type     | Rules    | Models |
| ---- | ---- | ------ |
| account-switch | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account    |        |
| failed-logon   | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive |        |