Rules by Product and UseCase
============================
Vendor: AppSense
----------------
### Product: [AppSense Application Manager](../ds_appsense_appsense_application_manager.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  10   |   4    |         3          |       2        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| alert-iot     | <b>T1078 - Valid Accounts</b><br> ↳ <b>A-SA-AN-ALERT-IOT-F</b>: First security alert name on the IOT/OT device<br> ↳ <b>A-SA-AN-ALERT-IOT-A</b>: Abnormal security alert name on IOT/OT Devices<br> ↳ <b>A-SA-OA-ALERT-IOT-A</b>: Abnormal IOT/OT device triggering security alert for organization    |  • <b>A-SA-OA-ALERT-IOT</b>: IOT/OT devices triggering security alerts in the organization<br> • <b>A-SA-AN-ALERT-IOT</b>: Security alert names on IOT/OT devices |
| process-alert | <b>TA0002 - TA0002</b><br> ↳ <b>EPA-UP-ALERT-F</b>: First security alert for executing this process by the user<br> ↳ <b>EPA-UP-ALERT-A</b>: Abnormal security alert for executing this process by the user<br> ↳ <b>EPA-UP-ALERT-N</b>: Common security alert for executing this process by the user<br> ↳ <b>EPA-UH-Pen-F</b>: Known pentest tool used<br><br><b>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools</b><br> ↳ <b>A-ALERT-Other</b>: Alert on asset<br> ↳ <b>A-ALERT-Critical</b>: Security Alert on a critical asset<br> ↳ <b>A-ALERT-Log4j</b>: Alert associated with an exploitation or post exploitation as seen with Log4j Vulnerability was detected. |  • <b>EPA-UH-Pen</b>: Malicious tools used by user<br> • <b>EPA-UP-ALERT</b>: Processes that triggered alerts for the user    |