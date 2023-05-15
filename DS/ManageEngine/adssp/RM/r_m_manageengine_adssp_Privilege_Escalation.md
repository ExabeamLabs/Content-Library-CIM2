Rules by Product and UseCase
============================
Vendor: ManageEngine
--------------------
### Product: [ADSSP](../ds_manageengine_adssp.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         1          |       1        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| aws-policy-write | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-AdminPolicy</b>: A critical policy with admin permissions was created in AWS<br> ↳ <b>AWS-UserCreatePolicyAdmin-Org-F</b>: First time this user created an administrative policy in AWS |  • <b>AWS-UserCreatePolicyAdmin-Org</b>: AWS users who created a critical policy |