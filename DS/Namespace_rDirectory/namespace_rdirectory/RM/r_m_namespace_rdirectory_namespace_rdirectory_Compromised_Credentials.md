Rules by Product and UseCase
============================
Vendor: Namespace rDirectory
----------------------------
### Product: [Namespace rDirectory](../ds_namespace_rdirectory_namespace_rdirectory.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   1    |         4          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| ds-access  | <b>T1207 - Rogue Domain Controller</b><br> ↳ <b>DS-DCSh-Add</b>: Directory service server object added<br> ↳ <b>DS-DCSh-Del</b>: Directory service server object created and deleted<br> ↳ <b>A-DS-DCShadow</b>: Possible DCShadow attack by asset detected.<br><br><b>T1003 - OS Credential Dumping</b><br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host.<br> ↳ <b>A-DCSync</b>: Possible DCSync attack detected<br><br><b>T1003.006 - OS Credential Dumping: DCSync</b><br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host.<br> ↳ <b>A-DCSync</b>: Possible DCSync attack detected<br><br><b>T1558 - Steal or Forge Kerberos Tickets</b><br> ↳ <b>ATP-AS-REP-2</b>: Suspicious UAC directory service change indicating AS-REP Roasting |  • <b>DS-HOSTS</b>: Models hosts in an Active Directory environment |