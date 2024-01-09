Rules by Product and UseCase
============================
Vendor: Cylance
---------------
### Product: [Cylance OPTICS](../ds_cylance_cylance_optics.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       2        |    7    |

| Event Type | Rules    | Models |
| ---------- | ---- | ------ |
| app-login  | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account     |        |
| file-alert | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |        |