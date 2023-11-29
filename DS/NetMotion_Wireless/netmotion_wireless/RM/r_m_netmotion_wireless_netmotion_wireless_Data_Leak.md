Rules by Product and UseCase
============================
Vendor: NetMotion Wireless
--------------------------
### Product: [NetMotion Wireless](../ds_netmotion_wireless_netmotion_wireless.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   2    |         2          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1133 - External Remote Services</b><br> ↳ <b>VPN-BSum</b>: Abnormal amount of data uploaded during VPN Session<br><br><b>T1052 - Exfiltration Over Physical Medium</b><br> ↳ <b>PR-NPSum</b>: Abnormal number of pages printed |  • <b>VPN-BSum</b>: Sum of bytes uploaded during VPN<br> • <b>PR-NPSum</b>: Number of pages printed by user |