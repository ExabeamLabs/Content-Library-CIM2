Rules by Product and UseCase
============================
Vendor: Synology NAS
--------------------
### Product: [Synology NAS](../ds_synology_nas_synology_nas.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   3    |         1          |       1        |    1    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| share-access | <b>T1021.002 - Remote Services: SMB/Windows Admin Shares</b><br> ↳ <b>SA-OU-F</b>: First admin share access for user in the organization<br> ↳ <b>SA-OU-A</b>: Abnormal admin share access for user in the organization<br> ↳ <b>SA-OH-F</b>: First admin share on this host<br> ↳ <b>SA-OH-A</b>: Abnormal admin share on this host<br> ↳ <b>SA-AsU-F</b>: First access of admin share on this host<br> ↳ <b>SA-AsU-A</b>: Abnormal access of admin share on this host |  • <b>SA-AsU</b>: Users accessing this Admin share<br> • <b>SA-OH</b>: Assets on which admin share is accessed in organization<br> • <b>SA-OU</b>: Users accessing admin share in the organization |