Vendor: CyberArk
================
### Product: [Endpoint Privilege Management](../ds_cyberark_endpoint_privilege_management.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  11   |   7    |     2      |       3        |    3    |

| Event Type        | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity      | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-F-SA-NC</b>: New service account access to application<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions<br> • <b>APP-AT-PRIV</b>: Privileged application activities    |
| privileged-access | <b>T1078 - Valid Accounts</b><br> ↳ <b>WPA-OU-F</b>: First privileged access event for user for organization<br> ↳ <b>WPA-OG-F</b>: First privileged access event for user for peer group<br> ↳ <b>WPA-UH-F</b>: First privileged access event on host for user<br> ↳ <b>WPA-HZ-F</b>: First privileged access event on host from zone<br> ↳ <b>WPA-USH-F</b>: First privileged access event on source host for user    |  • <b>WPA-USH</b>: Source hosts with privileged access events for user<br> • <b>WPA-HZ</b>: Source zones with privileged access events for host<br> • <b>WPA-UH</b>: Hosts with privileged access events for user<br> • <b>WPA-OG</b>: Privileged access activity for users in the peer group<br> • <b>WPA-OU</b>: Privileged access activity for users in the organization |