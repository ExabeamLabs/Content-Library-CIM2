Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - DNSServer](../ds_microsoft_event_viewer_-_dnsserver.md)
### Use-Case: [Data Access](../../../../UseCases/uc_data_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  19   |   11   |         1          |       1        |    8    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-UApp-F</b>: First login or activity within an application for user<br> ↳ <b>APP-UApp-A</b>: Abnormal login or activity within an application for user<br> ↳ <b>APP-AppU-F</b>: First login to an application for a user with no history<br> ↳ <b>APP-AppG-F</b>: First login to an application for group<br> ↳ <b>APP-GApp-A</b>: Abnormal login to an application for group<br> ↳ <b>APP-UOb-F</b>: First access to application object for user<br> ↳ <b>APP-UOb-A</b>: Abnormal access to application object for user<br> ↳ <b>APP-UappA-F</b>: First application activity for user<br> ↳ <b>APP-UappA-A</b>: Abnormal application activity for user<br> ↳ <b>APP-GappA-F</b>: First application activity for peer group<br> ↳ <b>APP-GappA-A</b>: Abnormal application activity for peer group<br> ↳ <b>APP-AA-F</b>: First application activity in the organization<br> ↳ <b>APP-AA-A</b>: Abnormal activity in application for the organization<br> ↳ <b>APP-UMime-F</b>: First mime type for user<br> ↳ <b>APP-UMime-A</b>: Abnormal mime type for user<br> ↳ <b>APP-GMime-F</b>: First mime type for peer group<br> ↳ <b>APP-GMime-A</b>: Abnormal mime type for peer group<br> ↳ <b>APP-OMime-F</b>: First mime type for organization<br> ↳ <b>APP-OMime-A</b>: Abnormal mime type for organization |  • <b>APP-OMime</b>: Mime types for organization<br> • <b>APP-GMime</b>: Mime types per peer group<br> • <b>APP-UMime</b>: Mime types per user<br> • <b>APP-AA</b>: Activity per application<br> • <b>APP-GappA</b>: Application activity per peer group<br> • <b>APP-UappA</b>: Application activity per user<br> • <b>APP-UOb</b>: Application objects per user<br> • <b>APP-GApp</b>: Group Logons to Applications<br> • <b>APP-AppG</b>: Groups per Application<br> • <b>APP-AppU</b>: User Logons to Applications<br> • <b>APP-UApp</b>: Applications per User |