Rules by Product and UseCase
============================
Vendor: Pharos
--------------
### Product: [Pharos](../ds_pharos_pharos.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   2    |         1          |       1        |    1    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| print-activity | <b>T1052 - Exfiltration Over Physical Medium</b><br> ↳ <b>PR-UP-F</b>: First print activity from printer for user<br> ↳ <b>PR-UP-A</b>: Abnormal printer for user<br> ↳ <b>PR-UT-TOW</b>: Abnormal print activity time for user<br> ↳ <b>PR-SRC-CODE</b>: Printed document with source code file extension |  • <b>PR-UT-TOW</b>: Print activity time for user<br> • <b>PR-UP</b>: Printers for user |