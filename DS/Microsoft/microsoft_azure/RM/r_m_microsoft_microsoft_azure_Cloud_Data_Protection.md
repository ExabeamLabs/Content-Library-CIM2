Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft Azure](../ds_microsoft_microsoft_azure.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   3    |         2          |       3        |    3    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| azure-disk-write     | <b>TA0009 - TA0009</b><br> ↳ <b>Azure-UserDiskFromSnapshot-Org-F</b>: First time Azure disk creation from snapshot         |  • <b>Azure-UserDiskFromSnapshot-Org</b>: Azure - users who created disks from snapshots |
| azure-snapshot-write | <b>TA0009 - TA0009</b><br> ↳ <b>Azure-UserSnapshotWrite-Org-F</b>: First time Azure snapshot write operation    |  • <b>Azure-UserSnapshotWrite-Org</b>: Azure - users who created/updated snapshots       |
| gcp-storage-list     | <b>T1580 - T1580</b><br> ↳ <b>GCP-UserStorageList-Org-F</b>: First time enumeration of storage buckets or objects for user |  • <b>GCP-UserStorageList-Org</b>: Users who listed storage buckets and objects in GCP   |