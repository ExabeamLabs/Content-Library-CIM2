Rules by Product and UseCase
============================
Vendor: MasterSAM
-----------------
### Product: [MasterSAM PAM](../ds_mastersam_mastersam_pam.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  17   |   9    |         3          |       2        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-successful | <b>T1078 - Valid Accounts</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br> ↳ <b>UA-UC-new</b>: Abnormal country for user by new user<br> ↳ <b>UA-GC-new</b>: Abnormal country for group by new user<br> ↳ <b>UA-OC-new</b>: Abnormal country for organization by new user<br> ↳ <b>UA-UC-Suspicious</b>: Activity from suspicious country<br> ↳ <b>UA-UC-Two</b>: Activity from two different countries<br> ↳ <b>UA-UC-Three</b>: Activity from 3 different countries<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br> ↳ <b>UA-UC-new</b>: Abnormal country for user by new user<br> ↳ <b>UA-GC-new</b>: Abnormal country for group by new user<br> ↳ <b>UA-OC-new</b>: Abnormal country for organization by new user<br> ↳ <b>UA-UC-Suspicious</b>: Activity from suspicious country<br> ↳ <b>UA-UC-Two</b>: Activity from two different countries<br> ↳ <b>UA-UC-Three</b>: Activity from 3 different countries |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity<br> • <b>UA-UI-new</b>: ISP of users during application activity    |
| database-login    | <b>T1213 - Data from Information Repositories</b><br> ↳ <b>DB-DbU-F</b>: First access to database for user<br> ↳ <b>DB-DbU-A</b>: Abnormal access to database for user<br> ↳ <b>DB-DbG-F</b>: First access to database for peer group<br> ↳ <b>DB-DbG-A</b>: Abnormal access to database for peer group<br> ↳ <b>DB-UDbZ-F</b>: First database activity from source zone per user, database<br> ↳ <b>DB-UDbZ-A</b>: Abnormal database activity from source zone per user, database<br> ↳ <b>DB-UDbH-F</b>: First database activity from host per user, database<br> ↳ <b>DB-UDbH-A</b>: Abnormal database activity from host per user, database<br> ↳ <b>DB-UDbI-F</b>: First database activity from IP per user, database<br> ↳ <b>DB-UDbI-A</b>: Abnormal database activity from IP per user, database    |  • <b>DB-UDbI</b>: Database activity from source IP per user, database<br> • <b>DB-UDbH</b>: Database activity from host per user, database<br> • <b>DB-UDbZ</b>: Database activity from source zone per user, database<br> • <b>DB-DbG</b>: Peer groups per database<br> • <b>DB-DbU</b>: Users per database |