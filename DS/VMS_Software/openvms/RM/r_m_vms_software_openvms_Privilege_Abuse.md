Rules by Product and UseCase
============================
Vendor: VMS Software
--------------------
### Product: [OpenVMS](../ds_vms_software_openvms.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   6    |         1          |       2        |    1    |

| Event Type        | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon      | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account    |  • <b>AE-UA</b>: All activity for users    |
| privileged-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>WPA-OU-F</b>: First privileged access event for user for organization<br> ↳ <b>WPA-OG-F</b>: First privileged access event for user for peer group<br> ↳ <b>WPA-UH-F</b>: First privileged access event on host for user<br> ↳ <b>WPA-HZ-F</b>: First privileged access event on host from zone<br> ↳ <b>WPA-USH-F</b>: First privileged access event on source host for user |  • <b>WPA-USH</b>: Source hosts with privileged access events for user<br> • <b>WPA-HZ</b>: Source zones with privileged access events for host<br> • <b>WPA-UH</b>: Hosts with privileged access events for user<br> • <b>WPA-OG</b>: Privileged access activity for users in the peer group<br> • <b>WPA-OU</b>: Privileged access activity for users in the organization |