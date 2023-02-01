Rules by Product and UseCase
============================
Vendor: Rubrik
--------------
### Product: [Rubrik Cloud Data Management](../ds_rubrik_rubrik_cloud_data_management.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       2        |    2    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| app-activity | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |