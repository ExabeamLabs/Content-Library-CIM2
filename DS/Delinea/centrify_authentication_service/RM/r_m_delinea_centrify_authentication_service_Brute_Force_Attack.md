Rules by Product and UseCase
============================
Vendor: Delinea
---------------
### Product: [Centrify Authentication Service](../ds_delinea_centrify_authentication_service.md)
### Use-Case: [Brute Force Attack](../../../../UseCases/uc_brute_force_attack.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       1        |    1    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| failed-logon | <b>T1021.001 - Remote Services: Remote Desktop Protocol</b><br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user<br><br><b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-08</b>: Abnormal number of failed logons for this user<br> ↳ <b>SEQ-UH-14</b>: Failed logon due to bad credentials<br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user |        |