Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco Network Monitoring and Analytics](../ds_cisco_cisco_network_monitoring_and_analytics.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         1          |       1        |    2    |

| Event Type         | Rules    | Models    |
| ---- | ---- | ---- |
| netflow-connection | <b>T1046 - Network Service Scanning</b><br> ↳ <b>A-NETFLOW-OsH-SweepScan-A</b>: Abnormal for asset to access 20 assets in 10 seconds |  • <b>A-NETFLOW-OsH-Scanners</b>: Assets that access multiple assets within seconds in the organization |