Rules by Product and UseCase
============================
Vendor: Check Point
-------------------
### Product: [Check Point Endpoint Security](../ds_check_point_check_point_endpoint_security.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         4          |       2        |    6    |

| Event Type     | Rules    | Models |
| ---- | ---- | ------ |
| security-alert | <b>T1027 - Obfuscated Files or Information</b><br> ↳ <b>A-ALERT-DL</b>: DL Correlation rule alert on asset<br> ↳ <b>A-ALERT-Correlation-Rule</b>: Correlation rule alert on asset<br><br><b>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools</b><br> ↳ <b>A-ALERT-DL</b>: DL Correlation rule alert on asset<br> ↳ <b>A-ALERT-Correlation-Rule</b>: Correlation rule alert on asset |        |
| vpn-login      | <b>T1090 - Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |        |