Rules by Product and UseCase
============================
Vendor: Exabeam
---------------
### Product: [Audit Log](../ds_exabeam_audit_log.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         1          |       1        |    1    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| aws-role-write | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserCreateRole-Org-F</b>: First time this user has performed role creation. |  • <b>AWS-UserCreateRole-Org</b>: AWS users who created roles in the organization |