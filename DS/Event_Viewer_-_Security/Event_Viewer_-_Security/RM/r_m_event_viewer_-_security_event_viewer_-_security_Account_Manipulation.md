Vendor: Event Viewer - Security
===============================
### Product: [Event Viewer - Security](../ds_event_viewer_-_security_event_viewer_-_security.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  15   |   8    |     1      |       5        |    5    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| member-removed | <b>T1098 - Account Manipulation</b><br> ↳ <b>GM-LocUA-F-new</b>: First group management activity by a new local user<br> ↳ <b>GM-LocUA-A</b>: Abnormal group management activity by local user<br> ↳ <b>GM-UH-F</b>: First group management activity from asset for user<br> ↳ <b>GM-UH-A</b>: Abnormal group management activity from asset for user<br> ↳ <b>GM-OZ-F</b>: First group management activity from network zone<br> ↳ <b>GM-OZ-A</b>: Abnormal group management activity from network zone<br> ↳ <b>GM-OH-F</b>: First group management activity from asset in the organization<br> ↳ <b>GM-OH-A</b>: Abnormal group management activity from asset in the organization<br> ↳ <b>GM-UT-TOW-A</b>: Abnormal day for user to perform group management activity<br> ↳ <b>AM-UA-MA-F</b>: First account group management activity for user<br> ↳ <b>AM-GA-MA-F</b>: First account group management activity for peer group<br> ↳ <b>AM-OU-SS-F</b>: First addition and removal of member from a group by user in a single session for organization<br> ↳ <b>AM-OU-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the organization<br> ↳ <b>AM-OG-SS-F</b>: First addition and removal of member from a group by user in a single session for peer group<br> ↳ <b>AM-OG-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the peer group |  • <b>AM-OG-SS</b>: Models the peer groups who perform addition and removal of members from group in same session<br> • <b>AM-OU-SS</b>: Models the users who perform addition and removal of members from group in same session in the organization<br> • <b>AE-GA</b>: All activity for peer groups<br> • <b>AE-UA</b>: All activity for users<br> • <b>GM-UT-TOW</b>: Group management activity time for user<br> • <b>GM-OH</b>: Group management hosts in organization<br> • <b>GM-OZ</b>: Group management activity from zone<br> • <b>GM-UH</b>: Group management activity on host for user |