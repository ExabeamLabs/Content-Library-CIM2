Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor - VM Insights](../ds_microsoft_azure_monitor_-_vm_insights.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       1        |    1    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset<br> ↳ <b>EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run |        |