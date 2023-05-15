Rules by Product and UseCase
============================
Vendor: ManageEngine
--------------------
### Product: [ADSSP](../ds_manageengine_adssp.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   6    |         2          |       1        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| aws-policy-write | <b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>AWS-MFA-User-F</b>: First time AWS authentication without MFA for user<br> ↳ <b>AWS-Operation-User-F</b>: First time AWS operation for user<br> ↳ <b>AWS-Service-User-F</b>: First time AWS cloud service for user<br> ↳ <b>AWS-UserAgent-Org-F</b>: First time user agent seen in AWS for the organization<br><br><b>T1535 - Unused/Unsupported Cloud Regions</b><br> ↳ <b>AWS-Region-User-F</b>: First time AWS region for user<br> ↳ <b>AWS-Region-Org-F</b>: First time AWS region for organization |  • <b>AWS-UserAgent-Org</b>: AWS User agents seen in the organization<br> • <b>AWS-Service-User</b>: AWS Services operations per user<br> • <b>AWS-Operation-User</b>: AWS API operation per user<br> • <b>AWS-Region-Org</b>: AWS Region activity for the organization<br> • <b>AWS-Region-User</b>: AWS Region activity per user<br> • <b>AWS-MFA-User</b>: AWS operations MFA statuseses |