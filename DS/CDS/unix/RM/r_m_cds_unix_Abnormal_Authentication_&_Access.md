Rules by Product and UseCase
============================
Vendor: CDS
-----------
### Product: [Unix](../ds_cds_unix.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   3    |         2          |       3        |    3    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| account-lockout | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-01</b>: Account lockout on an asset that belongs to this user    |    |
| account-switch  | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users    |
| failed-logon    | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-09</b>: Abnormal time of the week for a failed logon for user<br> ↳ <b>SEQ-UH-10</b>: Failed logons had multiple reasons<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-03</b>: Failed logon to a top failed logon asset by user<br> ↳ <b>SEQ-UH-06</b>: Abnormal failed logon to asset by user<br> ↳ <b>SEQ-UH-07</b>: Failed logon to an asset that user has not previously accessed |  • <b>FL-UH</b>: All Failed Logons per user<br> • <b>FL-OH</b>: All Failed Logons in the organization |