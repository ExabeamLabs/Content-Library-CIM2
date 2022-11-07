Vendor: Microsoft
=================
### Product: [SQL Server](../ds_microsoft_sql_server.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  27   |   13   |     3      |       10       |   10    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity   | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions    |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| member-added   | <b>T1098 - Account Manipulation</b><br> ↳ <b>A-GM-DhU-system-F</b>: First group management by system account on asset<br> ↳ <b>GM-LocUA-F-new</b>: First group management activity by a new local user<br> ↳ <b>GM-LocUA-A</b>: Abnormal group management activity by local user<br> ↳ <b>MA-SELF</b>: User added themself to a group<br> ↳ <b>MA-PRIV-F-local</b>: First addition to privileged group by local user<br> ↳ <b>MA-PRIV-A</b>: Abnormal addition to privileged group by user<br> ↳ <b>GM-UH-F</b>: First group management activity from asset for user<br> ↳ <b>GM-UH-A</b>: Abnormal group management activity from asset for user<br> ↳ <b>GM-OZ-F</b>: First group management activity from network zone<br> ↳ <b>GM-OZ-A</b>: Abnormal group management activity from network zone<br> ↳ <b>GM-OH-F</b>: First group management activity from asset in the organization<br> ↳ <b>GM-OH-A</b>: Abnormal group management activity from asset in the organization<br> ↳ <b>GM-UT-TOW-A</b>: Abnormal day for user to perform group management activity<br> ↳ <b>AM-GA-MA-F</b>: First account group management activity for peer group<br> ↳ <b>AM-OU-SS-F</b>: First addition and removal of member from a group by user in a single session for organization<br> ↳ <b>AM-OU-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the organization<br> ↳ <b>AM-OG-SS-F</b>: First addition and removal of member from a group by user in a single session for peer group<br> ↳ <b>AM-OG-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the peer group<br> ↳ <b>AM-OG-F</b>: First member addition to this group for the organization<br> ↳ <b>AM-OG-A</b>: Abnormal account addition to this group for the organization<br> ↳ <b>AM-GOU-F</b>: First account OU addition to this group<br> ↳ <b>AM-GOU-A</b>: Abnormal account OU addition to this group<br> ↳ <b>AM-UA-MA-F-new</b>: Account management activity for new user<br> ↳ <b>AM-GA-new</b>: First account management activity for group of a new user<br><br><b>T1136 - Create Account</b><br> ↳ <b>AM-UA-MA-F-new</b>: Account management activity for new user<br> ↳ <b>AM-GA-new</b>: First account management activity for group of a new user |  • <b>AE-GA</b>: All activity for peer groups<br> • <b>AM-GOU</b>: Account management, OUs that are added to security groups<br> • <b>AM-AG</b>: Account management, groups which users are being added to<br> • <b>AM-OG-SS</b>: Models the peer groups who perform addition and removal of members from group in same session<br> • <b>AM-OU-SS</b>: Models the users who perform addition and removal of members from group in same session in the organization<br> • <b>AE-UA</b>: All activity for users<br> • <b>GM-UT-TOW</b>: Group management activity time for user<br> • <b>GM-OH</b>: Group management hosts in organization<br> • <b>GM-OZ</b>: Group management activity from zone<br> • <b>GM-UH</b>: Group management activity on host for user<br> • <b>AM-OU-PG</b>: Account group management of high privileges in the organization<br> • <b>A-GM-DhU-system</b>: System accounts performing group management activities |
| member-removed | <b>T1098 - Account Manipulation</b><br> ↳ <b>GM-LocUA-F-new</b>: First group management activity by a new local user<br> ↳ <b>GM-LocUA-A</b>: Abnormal group management activity by local user<br> ↳ <b>GM-UH-F</b>: First group management activity from asset for user<br> ↳ <b>GM-UH-A</b>: Abnormal group management activity from asset for user<br> ↳ <b>GM-OZ-F</b>: First group management activity from network zone<br> ↳ <b>GM-OZ-A</b>: Abnormal group management activity from network zone<br> ↳ <b>GM-OH-F</b>: First group management activity from asset in the organization<br> ↳ <b>GM-OH-A</b>: Abnormal group management activity from asset in the organization<br> ↳ <b>GM-UT-TOW-A</b>: Abnormal day for user to perform group management activity<br> ↳ <b>AM-UA-MA-F</b>: First account group management activity for user<br> ↳ <b>AM-GA-MA-F</b>: First account group management activity for peer group<br> ↳ <b>AM-OU-SS-F</b>: First addition and removal of member from a group by user in a single session for organization<br> ↳ <b>AM-OU-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the organization<br> ↳ <b>AM-OG-SS-F</b>: First addition and removal of member from a group by user in a single session for peer group<br> ↳ <b>AM-OG-SS-A</b>: Abnormal addition and removal of member from a group in a single session in the peer group    |  • <b>AM-OG-SS</b>: Models the peer groups who perform addition and removal of members from group in same session<br> • <b>AM-OU-SS</b>: Models the users who perform addition and removal of members from group in same session in the organization<br> • <b>AE-GA</b>: All activity for peer groups<br> • <b>AE-UA</b>: All activity for users<br> • <b>GM-UT-TOW</b>: Group management activity time for user<br> • <b>GM-OH</b>: Group management hosts in organization<br> • <b>GM-OZ</b>: Group management activity from zone<br> • <b>GM-UH</b>: Group management activity on host for user    |