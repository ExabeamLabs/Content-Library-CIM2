Vendor: Microsoft
=================
### Product: [Defender ATP](../ds_microsoft_defender_atp.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   0    |     2      |       4        |    4    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset<br> ↳ <b>Trickbot-Recon</b>: Trickbot malware domain recon activity |        |
| security-alert  | <b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |        |