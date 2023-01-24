Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [MSSQL](../ds_microsoft_mssql.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       10       |   10    |

| Event Type       | Rules    | Models |
| ---- | ---- | ------ |
| app-activity     | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost-Failed</b>: User authentication or login failure from a known ransomware IP |        |