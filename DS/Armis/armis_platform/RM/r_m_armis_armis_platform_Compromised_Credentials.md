Rules by Product and UseCase
============================
Vendor: Armis
-------------
### Product: [Armis Platform](../ds_armis_armis_platform.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         1          |       1        |    2    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| alert-iot  | <b>T1078 - Valid Accounts</b><br> ↳ <b>A-SA-AN-ALERT-IOT-F</b>: First security alert name on the IOT/OT device<br> ↳ <b>A-SA-AN-ALERT-IOT-A</b>: Abnormal security alert name on IOT/OT Devices<br> ↳ <b>A-SA-OA-ALERT-IOT-A</b>: Abnormal IOT/OT device triggering security alert for organization |  • <b>A-SA-OA-ALERT-IOT</b>: IOT/OT devices triggering security alerts in the organization<br> • <b>A-SA-AN-ALERT-IOT</b>: Security alert names on IOT/OT devices |