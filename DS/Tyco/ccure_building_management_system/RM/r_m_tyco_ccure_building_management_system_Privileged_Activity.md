Rules by Product and UseCase
============================
Vendor: Tyco
------------
### Product: [CCURE Building Management System](../ds_tyco_ccure_building_management_system.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       2        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account |        |
| failed-physical-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>FPA-DU</b>: Failed badge access by disabled user    |        |
| physical-access        | <b>T1078 - Valid Accounts</b><br> ↳ <b>PA-DU</b>: Badge access by disabled user    |        |