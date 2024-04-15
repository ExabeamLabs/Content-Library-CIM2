Rules by Product and UseCase
============================
Vendor: VMS Software
--------------------
### Product: [OpenVMS](../ds_vms_software_openvms.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   7    |         3          |       2        |    1    |

| Event Type        | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon      | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |    |
| privileged-access | <b>TA0002 - TA0002</b><br> ↳ <b>WPA-UP-F</b>: First privileged process for user<br> ↳ <b>WPA-UP-A</b>: Abnormal privileged process for user<br> ↳ <b>WPA-GP-F</b>: First privileged process for peer group<br> ↳ <b>WPA-GP-A</b>: Abnormal privileged process for peer group<br> ↳ <b>WPA-PD-F</b>: First directory for privileged process<br> ↳ <b>WPA-PD-A</b>: Abnormal directory for privileged process<br> ↳ <b>WPA-HP-F</b>: First privileged process for host<br> ↳ <b>WPA-HP-A</b>: Abnormal privileged process for host<br> ↳ <b>WPA-OP-F</b>: First privileged process for organization<br> ↳ <b>WPA-OP-A</b>: Abnormal privileged process for organization |  • <b>WPA-OP</b>: Processes for organization<br> • <b>WPA-HP</b>: Processes for host<br> • <b>WPA-PD</b>: Directories per process<br> • <b>WPA-GP</b>: Privileged processes for peer group<br> • <b>WPA-GP-All</b>: Processes for peer group<br> • <b>WPA-UP</b>: Privileged processes for user<br> • <b>WPA-UP-All</b>: Processes for user |