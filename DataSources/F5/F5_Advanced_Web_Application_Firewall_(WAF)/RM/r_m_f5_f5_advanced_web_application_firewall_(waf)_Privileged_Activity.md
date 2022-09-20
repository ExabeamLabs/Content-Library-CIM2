Vendor: F5
==========
### Product: [F5 Advanced Web Application Firewall (WAF)](../ds_f5_f5_advanced_web_application_firewall_(waf).md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   4   |   0    |     2      |       6        |    6    |

| Event Type          | Rules    | Models |
| ---- | ---- | ------ |
| account-switch      | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account    |        |
| dlp-email-alert-out | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |        |
| process-created     | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset<br> ↳ <b>Trickbot-Recon</b>: Trickbot malware domain recon activity |        |