Rules by Product and UseCase
============================
Vendor: Auth0
-------------
### Product: [Auth0](../ds_auth0_auth0.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  17   |   7    |         6          |       7        |   11    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-deleted         | <b>T1531 - Account Access Removal</b><br> ↳ <b>AM-UA-AD-F</b>: First account deletion activity for user    |  • <b>AE-UA</b>: All activity for users    |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-F-SA-NC</b>: New service account access to application    |    |
| failed-app-login        | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| failed-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account    |  • <b>AE-UA</b>: All activity for users    |
| remote-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UH-I</b>: Interactive logon using a service account<br> ↳ <b>SL-UH-A</b>: Abnormal access from asset for a service account<br> ↳ <b>AL-F-F-CS</b>: First logon to a critical system for user<br> ↳ <b>AL-F-A-CS</b>: Abnormal logon to a critical system for user<br> ↳ <b>AL-UH-CS-NC</b>: Logon to a critical system for a user with no information<br> ↳ <b>AL-OU-F-CS</b>: First logon to a critical system that user has not previously accessed<br> ↳ <b>AL-HT-PRIV</b>: Non-Privileged logon to privileged asset<br> ↳ <b>AL-HT-EXEC-new</b>: New user logon to executive asset<br> ↳ <b>DC18-new</b>: Account switch by new user<br><br><b>T1078.002 - T1078.002</b><br> ↳ <b>SL-UH-I</b>: Interactive logon using a service account<br> ↳ <b>SL-UH-A</b>: Abnormal access from asset for a service account |  • <b>AL-HT-EXEC</b>: Executive Assets<br> • <b>AL-HT-PRIV</b>: Privilege Users Assets<br> • <b>AL-OU-CS</b>: Logon to critical servers<br> • <b>RA-UH</b>: Assets accessed by this user remotely<br> • <b>AL-UsH</b>: Source hosts per User<br> • <b>IL-UH-SA</b>: Interactive logon hosts for service accounts |
| web-activity-allowed    | <b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity    |    |