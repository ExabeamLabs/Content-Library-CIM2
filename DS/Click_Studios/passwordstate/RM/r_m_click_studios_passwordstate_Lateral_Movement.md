Rules by Product and UseCase
============================
Vendor: Click Studios
---------------------
### Product: [Passwordstate](../ds_click_studios_passwordstate.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       2        |    2    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| app-activity    | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |
| authentication-successful | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |