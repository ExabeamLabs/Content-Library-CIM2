Rules by Product and UseCase
============================
Vendor: Fortinet
----------------
### Product: [Fortiweb Web Application Firewall](../ds_fortinet_fortiweb_web_application_firewall.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         2          |       2        |    2    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| web-activity-allowed | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain |        |
| web-activity-denied  | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain |        |