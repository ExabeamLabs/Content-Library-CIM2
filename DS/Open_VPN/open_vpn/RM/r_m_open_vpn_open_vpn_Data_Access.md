Rules by Product and UseCase
============================
Vendor: Open VPN
----------------
### Product: [Open VPN](../ds_open_vpn_open_vpn.md)
### Use-Case: [Data Access](../../../../UseCases/uc_data_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   2    |         2          |       1        |    4    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1110 - Brute Force</b><br> ↳ <b>APP-UFL-COUNT</b>: Abnormal number of failed application logins for user<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>APP-UOb-Number</b>: Abnormal number of application objects accessed for user |  • <b>APP-UFL-COUNT</b>: Count of failed application logins in a session<br> • <b>APP-UOb-Number</b>: Count of app objects accessed in a session |