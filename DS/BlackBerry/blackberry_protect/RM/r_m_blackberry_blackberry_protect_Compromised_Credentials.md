Rules by Product and UseCase
============================
Vendor: BlackBerry
------------------
### Product: [BlackBerry Protect](../ds_blackberry_blackberry_protect.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   1    |         3          |       3        |    3    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity   | <b>T1078 - Valid Accounts</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP    |  • <b>UA-UI-new</b>: ISP of users during application activity |
| app-login      | <b>T1078 - Valid Accounts</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP    |  • <b>UA-UI-new</b>: ISP of users during application activity |
| security-alert | <b>T1190 - Exploit Public Fasing Application</b><br> ↳ <b>Log4j-Vul-Alert</b>: Alert for the CVE-2021-44228 vulnerability<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SA-OU-ALERT-F</b>: First security alert triggered for this user in the organization<br> ↳ <b>SA-OU-ALERT-A</b>: Abnormal user triggering security alert in the organization<br> ↳ <b>SA-OG-ALERT-F</b>: First security alert triggered for peer group in the organization<br> ↳ <b>SA-OG-ALERT-A</b>: Abnormal peer group triggering security alert in the organization<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>ALERT-VPN</b>: Security Alert on asset accessed by this user during VPN session |    |