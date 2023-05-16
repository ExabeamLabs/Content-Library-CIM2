Rules by Product and UseCase
============================
Vendor: AVI Networks
--------------------
### Product: [Avi Networks Software Load Balancer](../ds_avi_networks_avi_networks_software_load_balancer.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         2          |       2        |    2    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| app-login     | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |        |
| logout-remote | <b>T1210 - Exploitation of Remote Services</b><br> ↳ <b>A-Suspicious-Bluekeep2</b>: The channel ms_t120 has been closed on this asset. |        |