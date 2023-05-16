Rules by Product and UseCase
============================
Vendor: Amazon
--------------
### Product: [AWS CloudTrail](../ds_amazon_aws_cloudtrail.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  17   |   12   |         5          |       13       |   13    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| aws-policy-attach     | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserAddIdentityPolicy-Org-F</b>: First time policy attachment to an identity for this user<br> ↳ <b>AWS-UserAddIdentityPolicyGlobal-Org-F</b>: First time critical (global) policy attachment for user<br> ↳ <b>AWS-UserAddIdentityPolicyCritical-Org-F</b>: First time critical policy added by user    |  • <b>AWS-UserAddIdentityPolicy-Org</b>: AWS - users who added or attached identity policies in the organization    |
| aws-policy-list       | <b>TA0007 - TA0007</b><br> ↳ <b>AWS-UserPermEnum-Org-F</b>: First time permissions enumeration for user    |  • <b>AWS-UserPermEnum-Org</b>: AWS - permissions enumerations for user in the organization    |
| aws-policy-write      | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-CriticalPolicy</b>: A critical policy was created in AWS<br> ↳ <b>AWS-UserAddIdentityPolicy-Org-F</b>: First time policy attachment to an identity for this user<br> ↳ <b>AWS-UserAddIdentityPolicyGlobal-Org-F</b>: First time critical (global) policy attachment for user<br> ↳ <b>AWS-UserAddIdentityPolicyCritical-Org-F</b>: First time critical policy added by user<br> ↳ <b>AWS-UserCreatePolicy-Org-F</b>: First time policy creation for user<br> ↳ <b>AWS-UserCreatePolicyCritical-Org-F</b>: First time critical policy creation for user<br> ↳ <b>AWS-UserCreatePolicyCriticalGlobal-Org-F</b>: First time critical (global) policy creation for user |  • <b>AWS-UserCreatePolicy-Org</b>: AWS - users who created a policy in the organization<br> • <b>AWS-UserAddIdentityPolicy-Org</b>: AWS - users who added or attached identity policies in the organization |
| aws-role-assume       | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserAssumeRole-Org-F</b>: First time this user assumed a role in AWS    |  • <b>AWS-UserAssumeRole-Org</b>: AWS - users who assumed/switched roles in the organization    |
| aws-role-assumepolicy | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserModifyAssumeRole-Org-F</b>: First time this user modified who can assume a role in AWS    |  • <b>AWS-UserModifyAssumeRole-Org</b>: AWS - users who modified assume role policies in the organization    |
| aws-role-write        | <b>TA0004 - TA0004</b><br> ↳ <b>AWS-UserCreateRole-Org-F</b>: First time this user has performed role creation.    |  • <b>AWS-UserCreateRole-Org</b>: AWS - users who created roles in the organization    |
| gcp-bucket-create     | <b>T1074 - Data Staged</b><br> ↳ <b>GCP-UserCreateBucket-Org-F</b>: First time storage bucket creation for user    |  • <b>GCP-UserCreateBucket-Org</b>: Users who created storage buckets in GCP    |
| gcp-compute-list      | <b>T1580 - T1580</b><br> ↳ <b>GCP-UserComputeList-Org-F</b>: First time enumeration of compute resources for user    |  • <b>GCP-UserComputeList-Org</b>: Users who listed storage resources in GCP    |
| gcp-disk-attach       | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserAttachDisks-Org-F</b>: First time disk attachment for user    |  • <b>GCP-UserAttachDisks-Org</b>: Users who attached disks in GCP    |
| gcp-disk-create       | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateFromSnapshot-Org-F</b>: First time instance/disk creation from a snapshot for user    |  • <b>GCP-UserCreateFromSnapshot-Org</b>: Users who performed disk and instance creations from snapshots in GCP    |
| gcp-instance-create   | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateFromSnapshot-Org-F</b>: First time instance/disk creation from a snapshot for user    |  • <b>GCP-UserCreateFromSnapshot-Org</b>: Users who performed disk and instance creations from snapshots in GCP    |
| gcp-snapshot-create   | <b>TA0009 - TA0009</b><br> ↳ <b>GCP-UserCreateSnapshot-Org-F</b>: First time snapshot creation for user    |  • <b>GCP-UserCreateSnapshot-Org</b>: Users who performed snapshot creations in GCP    |
| gcp-storage-list      | <b>T1580 - T1580</b><br> ↳ <b>GCP-UserStorageList-Org-F</b>: First time enumeration of storage buckets or objects for user    |  • <b>GCP-UserStorageList-Org</b>: Users who listed storage buckets and objects in GCP    |