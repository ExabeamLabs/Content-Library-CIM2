Rules by Product and UseCase
============================
Vendor: Admin By Request
------------------------
### Product: [Admin By Request](../ds_admin_by_request_admin_by_request.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  11   |   8    |         2          |       2        |    0    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| privileged-access        | <b>TA0002 - TA0002</b><br> ↳ <b>WPA-UP-F</b>: First privileged process for user<br> ↳ <b>WPA-UP-A</b>: Abnormal privileged process for user<br> ↳ <b>WPA-GP-F</b>: First privileged process for peer group<br> ↳ <b>WPA-GP-A</b>: Abnormal privileged process for peer group<br> ↳ <b>WPA-PD-F</b>: First directory for privileged process<br> ↳ <b>WPA-PD-A</b>: Abnormal directory for privileged process<br> ↳ <b>WPA-HP-F</b>: First privileged process for host<br> ↳ <b>WPA-HP-A</b>: Abnormal privileged process for host<br> ↳ <b>WPA-OP-F</b>: First privileged process for organization<br> ↳ <b>WPA-OP-A</b>: Abnormal privileged process for organization |  • <b>WPA-OP</b>: Processes for organization<br> • <b>WPA-HP</b>: Processes for host<br> • <b>WPA-PD</b>: Directories per process<br> • <b>WPA-GP</b>: Privileged processes for peer group<br> • <b>WPA-GP-All</b>: Processes for peer group<br> • <b>WPA-UP</b>: Privileged processes for user<br> • <b>WPA-UP-All</b>: Processes for user |
| privileged-object-access | <b>T1059.003 - T1059.003</b><br> ↳ <b>WPA-OH-F</b>: First execution of critical windows command using privileged access on this host in the organization    |  • <b>WPA-OH</b>: Assets on which critical windows commands are executed in the organization    |