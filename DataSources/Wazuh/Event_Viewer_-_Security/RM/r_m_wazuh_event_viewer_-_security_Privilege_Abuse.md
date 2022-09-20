Vendor: Wazuh
=============
### Product: [Event Viewer - Security](../ds_wazuh_event_viewer_-_security.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   2    |     1      |       2        |    2    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| ds-access  | <b>T1484 - Group Policy Modification</b><br> ↳ <b>DS-APRIV</b>: Non-Privileged user accessing privileged directory service attribute<br> ↳ <b>DS-UA</b>: First access to attribute for privileged user |  • <b>DS-UA</b>: Attributes per privileged user<br> • <b>DS-APRIV</b>: Privileged user attributes |