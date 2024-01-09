Rules by Product and UseCase
============================
Vendor: VMware
--------------
### Product: [VMware ESXi](../ds_vmware_vmware_esxi.md)
### Use-Case: [Data Access](../../../../UseCases/uc_data_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  15   |   9    |         2          |       2        |    9    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| app-login      | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-UApp-F</b>: First login or activity within an application for user<br> ↳ <b>APP-UApp-A</b>: Abnormal login or activity within an application for user<br> ↳ <b>APP-AppU-F</b>: First login to an application for a user with no history<br> ↳ <b>APP-AppG-F</b>: First login to an application for group<br> ↳ <b>APP-GApp-A</b>: Abnormal login to an application for group    |  • <b>APP-GApp</b>: Group Logons to Applications<br> • <b>APP-AppG</b>: Groups per Application<br> • <b>APP-AppU</b>: User Logons to Applications<br> • <b>APP-UApp</b>: Applications per User    |
| database-login | <b>T1213 - Data from Information Repositories</b><br> ↳ <b>DB-DbU-F</b>: First access to database for user<br> ↳ <b>DB-DbU-A</b>: Abnormal access to database for user<br> ↳ <b>DB-DbG-F</b>: First access to database for peer group<br> ↳ <b>DB-DbG-A</b>: Abnormal access to database for peer group<br> ↳ <b>DB-UDbZ-F</b>: First database activity from source zone per user, database<br> ↳ <b>DB-UDbZ-A</b>: Abnormal database activity from source zone per user, database<br> ↳ <b>DB-UDbH-F</b>: First database activity from host per user, database<br> ↳ <b>DB-UDbH-A</b>: Abnormal database activity from host per user, database<br> ↳ <b>DB-UDbI-F</b>: First database activity from IP per user, database<br> ↳ <b>DB-UDbI-A</b>: Abnormal database activity from IP per user, database |  • <b>DB-UDbI</b>: Database activity from source IP per user, database<br> • <b>DB-UDbH</b>: Database activity from host per user, database<br> • <b>DB-UDbZ</b>: Database activity from source zone per user, database<br> • <b>DB-DbG</b>: Peer groups per database<br> • <b>DB-DbU</b>: Users per database |