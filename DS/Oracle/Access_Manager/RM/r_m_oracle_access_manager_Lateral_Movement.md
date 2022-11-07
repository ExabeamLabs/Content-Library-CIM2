Vendor: Oracle
==============
### Product: [Access Manager](../ds_oracle_access_manager.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   6   |   2    |     3      |       4        |    4    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| app-login        | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |    |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| nac-logon        | <b>T1078 - Valid Accounts</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user<br> ↳ <b>NAC-UM-F</b>: First MAC for user<br> ↳ <b>NAC-UM-A</b>: Abnormal MAC for user<br><br><b>T1021 - Remote Services</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user |  • <b>NAC-UM</b>: MAC addresses for user<br> • <b>NAC-UL</b>: Network locations for user |