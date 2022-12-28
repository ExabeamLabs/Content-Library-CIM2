Rules by Product and UseCase
============================
Vendor: MasterSAM
-----------------
### Product: [CA Privileged Access Manager Server Control](../ds_mastersam_ca_privileged_access_manager_server_control.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   0    |     1      |       2        |    2    |

| Event Type   | Rules    | Models |
| ---- | ---- | ------ |
| app-activity | <b>T1114.003 - Email Collection: Email Forwarding Rule</b><br> ↳ <b>EM-InRule-EX</b>: User has created an inbox forwarding rule to forward email to an external domain email<br> ↳ <b>EM-InRule-Public</b>: User has created an inbox forwarding rule to forward email to a public email domain<br> ↳ <b>EM-InRule-Fin</b>: User has created an inbox forwarding rule to forward emails containing financial keywords |        |