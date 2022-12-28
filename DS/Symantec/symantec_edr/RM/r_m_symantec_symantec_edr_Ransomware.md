Rules by Product and UseCase
============================
Vendor: Symantec
----------------
### Product: [Symantec EDR](../ds_symantec_symantec_edr.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   1   |   0    |     1      |       4        |    4    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| app-activity    | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |
| authentication-successful | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP |        |