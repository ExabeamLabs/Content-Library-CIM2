Rules by Product and UseCase
============================
Vendor: Damballa
----------------
### Product: [Damballa Failsafe](../ds_damballa_damballa_failsafe.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         3          |       2        |    4    |

| Event Type       | Rules    | Models |
| ---- | ---- | ------ |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP |        |
| security-alert   | <b>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools</b><br> ↳ <b>A-ALERT-DL</b>: DL Correlation rule alert on asset<br> ↳ <b>A-ALERT-Correlation-Rule</b>: Correlation rule alert on asset    |        |