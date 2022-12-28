Rules by Product and UseCase
============================
Vendor: Rubrik
--------------
### Product: [Rubrik Cloud Data Management](../ds_rubrik_rubrik_cloud_data_management.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   1   |   0    |     1      |       4        |    4    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| app-activity | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |
| app-login    | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP |        |