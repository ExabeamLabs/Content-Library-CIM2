Rules by Product and UseCase
============================
Vendor: VMware
--------------
### Product: [Carbon Black CES](../ds_vmware_carbon_black_ces.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       8        |    8    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset<br> ↳ <b>EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run |        |