Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - PowerShell](../ds_microsoft_event_viewer_-_powershell.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   0    |     1      |       5        |    5    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset<br> ↳ <b>EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run |        |