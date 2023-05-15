Rules by Product and UseCase
============================
Vendor: ManageEngine
--------------------
### Product: [ADSSP](../ds_manageengine_adssp.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   2    |         1          |       1        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| aws-policy-write | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-CriticalPolicy</b>: A critical policy was created in AWS<br> ↳ <b>AWS-UserAddIdentityPolicy-Org-F</b>: First time policy attachment to an identity for this user<br> ↳ <b>AWS-UserAddIdentityPolicyGlobal-Org-F</b>: First time critical (global) policy attachment for user<br> ↳ <b>AWS-UserAddIdentityPolicyCritical-Org-F</b>: First time critical policy added by user<br> ↳ <b>AWS-UserCreatePolicy-Org-F</b>: First time policy creation for user<br> ↳ <b>AWS-UserCreatePolicyCritical-Org-F</b>: First time critical policy creation for user<br> ↳ <b>AWS-UserCreatePolicyCriticalGlobal-Org-F</b>: First time critical (global) policy creation for user |  • <b>AWS-UserCreatePolicy-Org</b>: AWS users who created a policy in the organization<br> • <b>AWS-UserAddIdentityPolicy-Org</b>: AWS users who added or attached identity policies in the organization |