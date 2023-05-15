Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor](../ds_microsoft_azure_monitor.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   3    |         2          |       3        |    3    |

| Event Type        | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity      | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| azure-role-assign | <b>TA0004 - TA0004</b><br> ↳ <b>Azure-UserRoleAssign-Org-F</b>: First time Azure role assignment for user    |  • <b>Azure-UserRoleAssign-Org</b>: Azure - users who created IAM role assignments    |
| azure-role-write  | <b>TA0004 - TA0004</b><br> ↳ <b>Azure-UserRoleDefinitionWrite-Org-F</b>: First time Azure role definition modification for user    |  • <b>Azure-UserRoleDefinitionWrite-Org</b>: Azure - Users who created/modified IAM role definitions |