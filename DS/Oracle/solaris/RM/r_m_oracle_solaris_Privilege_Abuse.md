Rules by Product and UseCase
============================
Vendor: Oracle
--------------
### Product: [Solaris](../ds_oracle_solaris.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   2    |         1          |       1        |    1    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| process-created | <b>T1136.001 - Create Account: Create: Local Account</b><br> ↳ <b>AC-OZ-CLI-F</b>: First zone on which account was created using CLI command<br> ↳ <b>AC-OH-CLI-F</b>: First host on which account was created using CLI command |  • <b>AC-OH-CLI</b>: Hosts on which account was created using CLI command<br> • <b>AC-OZ-CLI</b>: Zones on which account was created using CLI command |