Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor](../ds_microsoft_azure_monitor.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         1          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| azure-instance-write | <b>T1496 - Resource Hijacking</b><br> ↳ <b>Azure-UserVMWrite-Org-F</b>: First time Azure VM write operation |  • <b>Azure-UserVMWrite-Org</b>: Azure - users who created/updated VMs |