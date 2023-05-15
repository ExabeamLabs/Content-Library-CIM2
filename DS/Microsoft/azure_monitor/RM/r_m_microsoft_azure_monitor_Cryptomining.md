Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor](../ds_microsoft_azure_monitor.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         2          |       2        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| azure-instance-write | <b>T1496 - Resource Hijacking</b><br> ↳ <b>Azure-UserVMWrite-Org-F</b>: First time Azure VM write operation    |  • <b>Azure-UserVMWrite-Org</b>: Azure - users who created/updated VMs |
| web-activity-allowed | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-Shadow-Mining</b>: User has browsed to a known coinmining/shadowmining domain<br><br><b>T1496 - Resource Hijacking</b><br> ↳ <b>A-WEB-Shadow-Mining</b>: Host has browsed to a known coinmining/shadowmining domain<br> ↳ <b>WEB-Shadow-Mining</b>: User has browsed to a known coinmining/shadowmining domain |    |