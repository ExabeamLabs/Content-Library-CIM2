Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Brute Force Attack](../../../../UseCases/uc_brute_force_attack.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  10   |   0    |         4          |       2        |   94    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| account-lockout | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-02</b>: Account lockout on an asset that does not belong to this user    |        |
| failed-logon    | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-08</b>: Abnormal number of failed logons for this user<br> ↳ <b>SEQ-UH-14</b>: Failed logon due to bad credentials<br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user<br> ↳ <b>A-FL-MULTI-USERS-SRC</b>: The same host failed to login to multiple users<br> ↳ <b>A-FL-MULTI-USERS-S</b>: Multiple users failed to login (S)<br> ↳ <b>A-FL-MULTI-USERS-L</b>: Multiple users failed to login (L)<br> ↳ <b>A-FL-MULTI-USERS-M</b>: Multiple users failed to login (M)<br> ↳ <b>A-FL-MULTI-DEST-S</b>: Failed logins to multiple destinations from host (S)<br> ↳ <b>A-FL-MULTI-DEST-M</b>: Failed logins to multiple destinations from host (M)<br><br><b>T1110.003 - T1110.003</b><br> ↳ <b>A-FL-MULTI-USERS-SRC</b>: The same host failed to login to multiple users<br><br><b>T1021 - Remote Services</b><br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user<br><br><b>T1021.001 - Remote Services: Remote Desktop Protocol</b><br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user |        |