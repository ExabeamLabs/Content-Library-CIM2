Rules by Product and UseCase
============================
Vendor: Endgame
---------------
### Product: [Endgame EDR](../ds_endgame_endgame_edr.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   0    |         3          |       1        |    1    |

| Event Type     | Rules    | Models |
| ---- | ---- | ------ |
| security-alert | <b>T1190 - Exploit Public Fasing Application</b><br> ↳ <b>Log4j-Vul-Alert</b>: Alert for the CVE-2021-44228 vulnerability<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SA-OU-ALERT-F</b>: First security alert triggered for this user in the organization<br> ↳ <b>SA-OU-ALERT-A</b>: Abnormal user triggering security alert in the organization<br> ↳ <b>SA-OG-ALERT-F</b>: First security alert triggered for peer group in the organization<br> ↳ <b>SA-OG-ALERT-A</b>: Abnormal peer group triggering security alert in the organization<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>ALERT-VPN</b>: Security Alert on asset accessed by this user during VPN session |        |