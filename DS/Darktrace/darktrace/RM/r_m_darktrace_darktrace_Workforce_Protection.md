Rules by Product and UseCase
============================
Vendor: Darktrace
-----------------
### Product: [Darktrace](../ds_darktrace_darktrace.md)
### Use-Case: [Workforce Protection](../../../../UseCases/uc_workforce_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   1    |         2          |       1        |    1    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| dlp-email-alert-out | <b>T1048 - Exfiltration Over Alternative Protocol</b><br> ↳ <b>EM-Competition</b>: Email to competition<br> ↳ <b>EM-OutSpam-M</b>: Email sent to more recipients than usual, at least one external. (M)<br> ↳ <b>EM-OutSpam-L</b>: Email sent to more recipients than usual, at least one external. (L)<br> ↳ <b>EM-Personal-Job</b>: Email with job seeking keywords in subject is sent to personal email address from company email address<br><br><b>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol</b><br> ↳ <b>EM-Competition</b>: Email to competition<br> ↳ <b>EM-OutSpam-M</b>: Email sent to more recipients than usual, at least one external. (M)<br> ↳ <b>EM-OutSpam-L</b>: Email sent to more recipients than usual, at least one external. (L)<br> ↳ <b>EM-Personal-Job</b>: Email with job seeking keywords in subject is sent to personal email address from company email address |  • <b>EM-Recipients-usr</b>: Recipients per Email for user |