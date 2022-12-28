Rules by Product and UseCase
============================
Vendor: Google
--------------
### Product: [Cloud Platform](../ds_google_cloud_platform.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   2    |     1      |       15       |   15    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| aws-role-assumepolicy | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserModifyAssumeRole-Org-F</b>: First time this user modified who can assume a role in AWS |  • <b>AWS-UserModifyAssumeRole-Org</b>: AWS - users who modified assume role policies in the organization |
| aws-role-write        | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserCreateRole-Org-F</b>: First time this user has performed role creation.    |  • <b>AWS-UserCreateRole-Org</b>: AWS - users who created roles in the organization    |