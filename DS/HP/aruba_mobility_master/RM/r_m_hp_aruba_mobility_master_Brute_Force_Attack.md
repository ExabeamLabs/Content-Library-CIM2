Rules by Product and UseCase
============================
Vendor: HP
----------
### Product: [Aruba Mobility Master](../ds_hp_aruba_mobility_master.md)
### Use-Case: [Brute Force Attack](../../../../UseCases/uc_brute_force_attack.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         1          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1110 - Brute Force</b><br> ↳ <b>AUTH-F-COUNT</b>: Abnormal number of failed authentications during this user session |  • <b>AUTH-F-COUNT</b>: Count of failed authentication events in a session |