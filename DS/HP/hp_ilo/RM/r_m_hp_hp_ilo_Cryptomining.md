Rules by Product and UseCase
============================
Vendor: HP
----------
### Product: [HP iLO](../ds_hp_hp_ilo.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       1        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| web-activity-allowed | <b>T1496 - Resource Hijacking</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP<br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain<br> ↳ <b>A-NET-Coin-IP</b>: Connection to IP associated with cryptocurrency mining<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP |        |