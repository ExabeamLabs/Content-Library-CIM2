Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco Network Monitoring and Analytics](../ds_cisco_cisco_network_monitoring_and_analytics.md)
### Use-Case: [Data Exfiltration](../../../../UseCases/uc_data_exfiltration.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         4          |       1        |    2    |

| Event Type         | Rules    | Models |
| ---- | ---- | ------ |
| netflow-connection | <b>T1048 - Exfiltration Over Alternative Protocol</b><br> ↳ <b>A-NETFLOW-BitTorrent</b>: Asset accessed BitTorrent application<br><br><b>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol</b><br> ↳ <b>A-NETFLOW-BitTorrent</b>: Asset accessed BitTorrent application<br><br><b>T1071 - Application Layer Protocol</b><br> ↳ <b>A-NETFLOW-BitTorrent</b>: Asset accessed BitTorrent application<br><br><b>T1071.002 - Application Layer Protocol: File Transfer Protocols</b><br> ↳ <b>A-NETFLOW-BitTorrent</b>: Asset accessed BitTorrent application |        |