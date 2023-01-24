Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   2    |         2          |       87       |   87    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| aws-role-assumepolicy | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserModifyAssumeRole-Org-F</b>: First time this user modified who can assume a role in AWS   |  • <b>AWS-UserModifyAssumeRole-Org</b>: AWS - users who modified assume role policies in the organization       |
| gcp-instance-create   | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateFromSnapshot-Org-F</b>: First time instance/disk creation from a snapshot for user |  • <b>GCP-UserCreateFromSnapshot-Org</b>: Users who performed disk and instance creations from snapshots in GCP |