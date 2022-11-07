Vendor: Microsoft
=================
### Product: [Event Viewer - Securitys](../ds_microsoft_event_viewer_-_securitys.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   2    |     1      |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| ds-access  | <b>T1484 - Group Policy Modification</b><br> ↳ <b>DS-APRIV</b>: Non-Privileged user accessing privileged directory service attribute<br> ↳ <b>DS-UA</b>: First access to attribute for privileged user |  • <b>DS-UA</b>: Attributes per privileged user<br> • <b>DS-APRIV</b>: Privileged user attributes |