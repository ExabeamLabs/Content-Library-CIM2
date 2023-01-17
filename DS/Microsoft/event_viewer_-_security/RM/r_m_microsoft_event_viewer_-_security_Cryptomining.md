Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Cryptomining](../../../../UseCases/uc_cryptomining.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   1    |     2      |       87       |   87    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| gcp-instance-create | <b>T1074 - Data Staged</b><br> ↳ <b>GCP-UserCreateInstance-Org-F</b>: First time instance creation for user<br><br><b>T1496 - Resource Hijacking</b><br> ↳ <b>GCP-UserCreateInstance-Org-F</b>: First time instance creation for user |  • <b>GCP-UserCreateInstance-Org</b>: Users who created an instance in GCP |
| process-created     | <b>T1496 - Resource Hijacking</b><br> ↳ <b>A-EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run on this asset<br> ↳ <b>EPA-Shadow-Mining-name</b>: Process ending with 'miner.exe' has been run    |    |