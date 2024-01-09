Rules by Product and UseCase
============================
Vendor: Box
-----------
### Product: [Box Cloud Content Management](../ds_box_box_cloud_content_management.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         1          |       2        |    0    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| app-login     | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-F-SA-NC</b>: New service account access to application |        |
| file-download | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |        |