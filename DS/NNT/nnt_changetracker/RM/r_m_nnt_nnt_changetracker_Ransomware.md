Rules by Product and UseCase
============================
Vendor: NNT
-----------
### Product: [NNT ChangeTracker](../ds_nnt_nnt_changetracker.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   0    |     1      |       4        |    4    |

| Event Type       | Rules    | Models |
| ---- | ---- | ------ |
| app-login        | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost-Failed</b>: User authentication or login failure from a known ransomware IP |        |