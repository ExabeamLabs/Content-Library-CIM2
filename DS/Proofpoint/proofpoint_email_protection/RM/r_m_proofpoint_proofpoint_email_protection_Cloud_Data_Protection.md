Rules by Product and UseCase
============================
Vendor: Proofpoint
------------------
### Product: [Proofpoint Email Protection](../ds_proofpoint_proofpoint_email_protection.md)
### Use-Case: [Cloud Data Protection](../../../../UseCases/uc_cloud_data_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         1          |       1        |    1    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| azure-blob-read | <b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>B-Azure-UserAgent-StorageAccount-F</b>: First time user agent seen when accessing this Azure storage account |  • <b>B-Azure-UserAgent-StorageAccount</b>: Azure - user agents per storage account |