Rules by Product and UseCase
============================
Vendor: NCP
-----------
### Product: [NCP](../ds_ncp_ncp.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  13   |   2    |         2          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1078 - Valid Accounts</b><br> ↳ <b>AL-UHcount-S</b>: Abnormal number of logon assets (S)<br> ↳ <b>AL-UHcount-M</b>: Abnormal number of assets logged on within a session (M)<br> ↳ <b>AL-UHcount-L</b>: Abnormal number of assets logged on within a session (L)<br> ↳ <b>AL-OHcount</b>: Abnormal number of assets logged on within a session compared to the organization<br> ↳ <b>AL-GHcount</b>: Abnormal number of logged on assets compared to group<br> ↳ <b>RA-UHcount-S</b>: Abnormal number of accessed hosts for user (S)<br> ↳ <b>RA-UHcount-M</b>: Abnormal number of accessed hosts within a session for user (M)<br> ↳ <b>RA-UHcount-L</b>: Abnormal number of accessed hosts for user (L)<br> ↳ <b>RA-OHcount</b>: Abnormal number of accessed hosts within a session for the organization<br> ↳ <b>RA-GHcount</b>: Abnormal number of accessed assets for group<br> ↳ <b>DC08d-new</b>: Abnormal number of assets compared to group for a new user<br> ↳ <b>DC14g-new</b>: Abnormal number of accessed assets for group of new user<br> ↳ <b>DC17j-new</b>: Abnormal number of accessed zones for group of a new user<br><br><b>T1021 - Remote Services</b><br> ↳ <b>RA-UHcount-S</b>: Abnormal number of accessed hosts for user (S)<br> ↳ <b>RA-UHcount-M</b>: Abnormal number of accessed hosts within a session for user (M)<br> ↳ <b>RA-UHcount-L</b>: Abnormal number of accessed hosts for user (L)<br> ↳ <b>RA-OHcount</b>: Abnormal number of accessed hosts within a session for the organization<br> ↳ <b>RA-GHcount</b>: Abnormal number of accessed assets for group |  • <b>RA-OHcount</b>: Count of assets access per user in the organization<br> • <b>AL-OHcount</b>: Count of assets logon per user in the organization |