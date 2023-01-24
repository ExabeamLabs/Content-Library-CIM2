Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco](../ds_cisco_cisco.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         3          |       3        |    3    |

| Event Type          | Rules    | Models |
| ---- | ---- | ------ |
| app-activity        | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |        |
| app-activity-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP |        |
| logout-remote       | <b>T1210 - Exploitation of Remote Services</b><br> ↳ <b>A-Suspicious-Bluekeep2</b>: The channel ms_t120 has been closed on this asset.    |        |