Rules by Product and UseCase
============================
Vendor: Fortinet
----------------
### Product: [FortiNAC](../ds_fortinet_fortinac.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         4          |       2        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| local-logon   | <b>T1550 - Use Alternate Authentication Material</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected<br><br><b>T1550.003 - Use Alternate Authentication Material: Pass the Ticket</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected<br><br><b>T1558 - Steal or Forge Kerberos Tickets</b><br> ↳ <b>EXPERT-PENTEST-DOMAINS</b>: Possible credentials theft attack detected |        |
| logout-remote | <b>T1210 - Exploitation of Remote Services</b><br> ↳ <b>A-Suspicious-Bluekeep2</b>: The channel ms_t120 has been closed on this asset.    |        |