Rules by Product and UseCase
============================
Vendor: OneWelcome
------------------
### Product: [OneWelcome Cloud Identity Platform](../ds_onewelcome_onewelcome_cloud_identity_platform.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       3        |    3    |

| Event Type         | Rules    | Models |
| ---- | ---- | ------ |
| account-switch     | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account    |        |
| dlp-email-alert-in | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |        |
| process-created    | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset |        |