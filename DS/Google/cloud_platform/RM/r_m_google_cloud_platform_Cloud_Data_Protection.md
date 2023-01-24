Rules by Product and UseCase
============================
Vendor: Google
--------------
### Product: [Cloud Platform](../ds_google_cloud_platform.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   5    |         2          |       15       |   15    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| aws-role-assumepolicy | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserModifyAssumeRole-Org-F</b>: First time this user modified who can assume a role in AWS   |  • <b>AWS-UserModifyAssumeRole-Org</b>: AWS - users who modified assume role policies in the organization       |
| aws-role-write        | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserCreateRole-Org-F</b>: First time this user has performed role creation.    |  • <b>AWS-UserCreateRole-Org</b>: AWS - users who created roles in the organization    |
| gcp-disk-attach       | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserAttachDisks-Org-F</b>: First time disk attachment for user    |  • <b>GCP-UserAttachDisks-Org</b>: Users who attached disks in GCP    |
| gcp-disk-create       | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateFromSnapshot-Org-F</b>: First time instance/disk creation from a snapshot for user |  • <b>GCP-UserCreateFromSnapshot-Org</b>: Users who performed disk and instance creations from snapshots in GCP |
| gcp-instance-create   | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateFromSnapshot-Org-F</b>: First time instance/disk creation from a snapshot for user |  • <b>GCP-UserCreateFromSnapshot-Org</b>: Users who performed disk and instance creations from snapshots in GCP |
| gcp-snapshot-create   | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateSnapshot-Org-F</b>: First time snapshot creation for user    |  • <b>GCP-UserCreateSnapshot-Org</b>: Users who performed snapshot creations in GCP    |