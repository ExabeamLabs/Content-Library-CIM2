Rules by Product and UseCase
============================
Vendor: Password Manager Pro
----------------------------
### Product: [Password Manager Pro](../ds_password_manager_pro_password_manager_pro.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         2          |       1        |    1    |

| Event Type | Rules    | Models |
| ---------- | ---- | ------ |
| app-login  | <b>T1090 - Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |