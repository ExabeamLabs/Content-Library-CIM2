Rules by Product and UseCase
============================
Vendor: HashiCorp
-----------------
### Product: [Terraform](../ds_hashicorp_terraform.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       2        |    0    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| web-activity-allowed | <b>T1496 - Resource Hijacking</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP<br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain<br> ↳ <b>A-NET-Coin-IP</b>: Connection to IP associated with cryptocurrency mining<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP |        |
| web-activity-denied  | <b>T1496 - Resource Hijacking</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP<br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain<br> ↳ <b>A-NET-Coin-IP</b>: Connection to IP associated with cryptocurrency mining<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-Shadow-Mining-IP</b>: User has connected to a known coinmining/shadowmining IP |        |