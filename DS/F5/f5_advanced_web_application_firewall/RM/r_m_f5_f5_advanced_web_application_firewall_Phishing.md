Rules by Product and UseCase
============================
Vendor: F5
----------
### Product: [F5 Advanced Web Application Firewall](../ds_f5_f5_advanced_web_application_firewall.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         4          |       2        |    2    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| dlp-email-alert-out | <b>T1048 - Exfiltration Over Alternative Protocol</b><br> ↳ <b>EM-OD-A</b>: Abnormal email domain for organization<br><br><b>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol</b><br> ↳ <b>EM-OD-A</b>: Abnormal email domain for organization |  • <b>EM-OD</b>: Domains per organization |
| process-created     | <b>T1566 - Phishing</b><br> ↳ <b>A-Exec-Outlook-Temp</b>: A suspicious program was executed in the Outlook temp folder on this asset.<br><br><b>T1566.001 - T1566.001</b><br> ↳ <b>A-Exec-Outlook-Temp</b>: A suspicious program was executed in the Outlook temp folder on this asset.    |    |