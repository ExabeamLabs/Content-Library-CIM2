Rules by Product and UseCase
============================
Vendor: Barracuda
-----------------
### Product: [Barracuda Cloudgen Firewall](../ds_barracuda_barracuda_cloudgen_firewall.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       2        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| network-connection-failed     | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-NET-Coin-IP</b>: Connection to IP associated with cryptocurrency mining |        |
| network-connection-successful | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-NET-Coin-IP</b>: Connection to IP associated with cryptocurrency mining |        |