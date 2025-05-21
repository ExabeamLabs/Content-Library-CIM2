Rules by Product and UseCase
============================
Vendor: ESector
---------------
### Product: [ESector DEFESA Logger](../ds_esector_esector_defesa_logger.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   0    |         3          |       2        |    2    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| app-activity | <b>T1114 - Email Collection</b><br> ↳ <b>EM-InRule-EX</b>: User has created an inbox forwarding rule to forward email to an external domain email<br> ↳ <b>EM-InRule-Public</b>: User has created an inbox forwarding rule to forward email to a public email domain<br> ↳ <b>EM-InRule-Fin</b>: User has created an inbox forwarding rule to forward emails containing financial keywords<br><br><b>T1114.003 - Email Collection: Email Forwarding Rule</b><br> ↳ <b>EM-InRule-EX</b>: User has created an inbox forwarding rule to forward email to an external domain email<br> ↳ <b>EM-InRule-Public</b>: User has created an inbox forwarding rule to forward email to a public email domain<br> ↳ <b>EM-InRule-Fin</b>: User has created an inbox forwarding rule to forward emails containing financial keywords |        |
| file-write   | <b>T1114 - Email Collection</b><br> ↳ <b>FA-Outlook-pst</b>: A file ends with either  pst or ost<br><br><b>T1114.001 - T1114.001</b><br> ↳ <b>FA-Outlook-pst</b>: A file ends with either  pst or ost    |        |