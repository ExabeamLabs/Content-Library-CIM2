Rules by Product and UseCase
============================
Vendor: Fidelis
---------------
### Product: [Fidelis XPS](../ds_fidelis_fidelis_xps.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         2          |       1        |    0    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| dlp-email-alert-out | <b>T1048 - Exfiltration Over Alternative Protocol</b><br> ↳ <b>EM-OD-A</b>: Abnormal email domain for organization<br><br><b>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol</b><br> ↳ <b>EM-OD-A</b>: Abnormal email domain for organization |  • <b>EM-OD</b>: Domains per organization |