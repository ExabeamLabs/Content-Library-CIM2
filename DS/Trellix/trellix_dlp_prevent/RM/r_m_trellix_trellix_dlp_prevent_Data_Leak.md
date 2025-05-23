Rules by Product and UseCase
============================
Vendor: Trellix
---------------
### Product: [Trellix DLP Prevent](../ds_trellix_trellix_dlp_prevent.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         2          |       1        |    1    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| dlp-email-alert-out-failed | <b>T1048 - Exfiltration Over Alternative Protocol</b><br> ↳ <b>FEM-UD-R</b>: Repeated email failure to domain<br> ↳ <b>FEM-FU</b>: Emailing a previously failed attachment<br> ↳ <b>EM-BSum-5MB-Fail</b>: Failed attempt to email over 5MB of data to a personal email domain.<br><br><b>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol</b><br> ↳ <b>FEM-UD-R</b>: Repeated email failure to domain<br> ↳ <b>FEM-FU</b>: Emailing a previously failed attachment<br> ↳ <b>EM-BSum-5MB-Fail</b>: Failed attempt to email over 5MB of data to a personal email domain. |  • <b>FEM-FU</b>: Users per file names in failed outgoing emails<br> • <b>FEM-UD</b>: Failed Email Domains per User |