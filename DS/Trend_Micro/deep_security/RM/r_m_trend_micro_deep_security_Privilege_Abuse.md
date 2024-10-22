Rules by Product and UseCase
============================
Vendor: Trend Micro
-------------------
### Product: [Deep Security](../ds_trend_micro_deep_security.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  14   |   8    |         9          |       4        |    2    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account    |  • <b>AE-UA</b>: All activity for users    |
| process-created | <b>T1136 - Create Account</b><br> ↳ <b>NET-EXE-ADD-GRP-ORG-F</b>: First time net.exe has been used to create/add to a group by this user.<br> ↳ <b>NET-EXE-ADD-GRP-ORG-A</b>: Abnormal usage of net.exe to create/add to a group by this user.<br> ↳ <b>AC-OZ-CLI-F</b>: First zone on which account was created using CLI command<br> ↳ <b>AC-OH-CLI-F</b>: First host on which account was created using CLI command<br><br><b>T1136.001 - Create Account: Create: Local Account</b><br> ↳ <b>AC-OZ-CLI-F</b>: First zone on which account was created using CLI command<br> ↳ <b>AC-OH-CLI-F</b>: First host on which account was created using CLI command<br><br><b>T1047 - Windows Management Instrumentation</b><br> ↳ <b>WMIC-EXE-RENAME-ORG-F</b>: First time WMIC.exe has been used to rename a user account by this user.<br> ↳ <b>WMIC-EXE-RENAME-ORG-A</b>: Abnormal usage of WMIC.exe to rename a user account by this user.<br> ↳ <b>WMIC-EXE-RENAME-GRP-ORG-F</b>: First time WMIC.exe has been used to rename a group by this user.<br> ↳ <b>WMIC-EXE-RENAME-GRP-ORG-A</b>: Abnormal usage of WMIC.exe to rename a group by this user.<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>NET-EXE-ADD-GRP-ORG-F</b>: First time net.exe has been used to create/add to a group by this user.<br> ↳ <b>NET-EXE-ADD-GRP-ORG-A</b>: Abnormal usage of net.exe to create/add to a group by this user.<br> ↳ <b>NET-EXE-ACTIVE-ORG-F</b>: First time net.exe has been used to disable/enable a user account by this user.<br> ↳ <b>NET-EXE-ACTIVE-ORG-A</b>: Abnormal usage of net.exe to disable/enable a user account by this user.<br> ↳ <b>WMIC-EXE-RENAME-ORG-F</b>: First time WMIC.exe has been used to rename a user account by this user.<br> ↳ <b>WMIC-EXE-RENAME-ORG-A</b>: Abnormal usage of WMIC.exe to rename a user account by this user.<br> ↳ <b>WMIC-EXE-RENAME-GRP-ORG-F</b>: First time WMIC.exe has been used to rename a group by this user.<br> ↳ <b>WMIC-EXE-RENAME-GRP-ORG-A</b>: Abnormal usage of WMIC.exe to rename a group by this user.<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>NET-EXE-ADD-GRP-ORG-F</b>: First time net.exe has been used to create/add to a group by this user.<br> ↳ <b>NET-EXE-ADD-GRP-ORG-A</b>: Abnormal usage of net.exe to create/add to a group by this user.<br> ↳ <b>NET-EXE-ACTIVE-ORG-F</b>: First time net.exe has been used to disable/enable a user account by this user.<br> ↳ <b>NET-EXE-ACTIVE-ORG-A</b>: Abnormal usage of net.exe to disable/enable a user account by this user. |  • <b>AC-OH-CLI</b>: Hosts on which account was created using CLI command<br> • <b>AC-OZ-CLI</b>: Zones on which account was created using CLI command<br> • <b>WMIC-EXE-RENAME-GRP-ORG</b>: Using WMIC.exe to rename a group<br> • <b>WMIC-EXE-RENAME-ORG</b>: Using WMIC.exe to rename a user account<br> • <b>NET-EXE-ACTIVE-ORG</b>: Using net.exe to disable/enable a user account<br> • <b>NET-EXE-ADD-GRP-ORG</b>: Using net.exe to add a group account |
| service-created | <b>T1053 - Scheduled Task/Job</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1053.005 - Scheduled Task/Job: Scheduled Task</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543 - Create or Modify System Process</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset    |  • <b>AL-HT-PRIV</b>: Privilege Users Assets    |
| task-created    | <b>T1053 - Scheduled Task/Job</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1053.005 - Scheduled Task/Job: Scheduled Task</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543 - Create or Modify System Process</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset    |  • <b>AL-HT-PRIV</b>: Privilege Users Assets    |