Vendor: Lenel
=============
### Product: [OnGuard](../ds_lenel_onguard.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   0    |     1      |       2        |    2    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| failed-physical-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>FPA-DU</b>: Failed badge access by disabled user    |        |
| file-write    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |        |
| physical-access        | <b>T1078 - Valid Accounts</b><br> ↳ <b>PA-DU</b>: Badge access by disabled user    |        |