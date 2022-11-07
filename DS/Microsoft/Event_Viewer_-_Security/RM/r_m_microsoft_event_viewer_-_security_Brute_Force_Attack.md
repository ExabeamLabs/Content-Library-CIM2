Vendor: Microsoft
=================
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Brute Force Attack](../../../../UseCases/uc_brute_force_attack.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   1    |     1      |       90       |   90    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| account-lockout | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-02</b>: Account lockout on an asset that does not belong to this user         |    |
| vpn-logout      | <b>T1110 - Brute Force</b><br> ↳ <b>AUTH-F-COUNT</b>: Abnormal number of failed authentications during this user session |  • <b>AUTH-F-COUNT</b>: Count of failed authentication events in a session |