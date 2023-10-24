Rules by Product and UseCase
============================
Vendor: Palo Alto Networks
--------------------------
### Product: [Traps Endpoint Security Manager](../ds_palo_alto_networks_traps_endpoint_security_manager.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       2        |    2    |

| Event Type     | Rules    | Models |
| ---- | ---- | ------ |
| app-login      | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |        |
| security-alert | <b>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools</b><br> ↳ <b>A-ALERT-DL</b>: DL Correlation rule alert on asset<br> ↳ <b>A-ALERT-Correlation-Rule</b>: Correlation rule alert on asset |        |