Rules by Product and UseCase
============================
Vendor: Imperva
---------------
### Product: [Imperva SecureSphere](../ds_imperva_imperva_securesphere.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   2    |         2          |       2        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity          | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| aws-role-assumepolicy | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-RolePublicPolicy-Org-F</b>: First time this role was made public in AWS    |  • <b>AWS-RolePublicPolicy-Org</b>: AWS roles who were given a public assume policy |