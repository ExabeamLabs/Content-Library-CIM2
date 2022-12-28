Rules by Product and UseCase
============================
Vendor: Imperva
---------------
### Product: [Imperva SecureSphere](../ds_imperva_imperva_securesphere.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   1   |   0    |     1      |       12       |   12    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| app-activity | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |