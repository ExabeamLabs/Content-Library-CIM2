Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Application](../ds_microsoft_event_viewer_-_application.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   0    |     1      |       11       |   11    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset<br> ↳ <b>EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run |        |