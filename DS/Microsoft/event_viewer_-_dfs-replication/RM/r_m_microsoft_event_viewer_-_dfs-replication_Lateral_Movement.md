Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - DFS-Replication](../ds_microsoft_event_viewer_-_dfs-replication.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         2          |       1        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| authentication-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP |        |