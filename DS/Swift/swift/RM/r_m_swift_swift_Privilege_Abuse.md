Rules by Product and UseCase
============================
Vendor: Swift
-------------
### Product: [Swift](../ds_swift_swift.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   0    |         3          |       4        |    4    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |        |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-F-SA-NC</b>: New service account access to application    |        |
| failed-app-login        | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |        |
| vpn-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account |        |