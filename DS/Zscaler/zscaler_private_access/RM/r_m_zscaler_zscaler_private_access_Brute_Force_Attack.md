Rules by Product and UseCase
============================
Vendor: Zscaler
---------------
### Product: [Zscaler Private Access](../ds_zscaler_zscaler_private_access.md)
### Use-Case: [Brute Force Attack](../../../../UseCases/uc_brute_force_attack.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         1          |       2        |    2    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| account-lockout | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-02</b>: Account lockout on an asset that does not belong to this user         |    |
| vpn-logout      | <b>T1110 - Brute Force</b><br> ↳ <b>AUTH-F-COUNT</b>: Abnormal number of failed authentications during this user session |  • <b>AUTH-F-COUNT</b>: Count of failed authentication events in a session |