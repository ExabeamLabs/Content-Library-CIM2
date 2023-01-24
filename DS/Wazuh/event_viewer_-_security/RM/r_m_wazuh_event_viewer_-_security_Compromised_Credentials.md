Rules by Product and UseCase
============================
Vendor: Wazuh
-------------
### Product: [Event Viewer - Security](../ds_wazuh_event_viewer_-_security.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  10   |   2    |         4          |       2        |    2    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| ds-access    | <b>T1207 - Rogue Domain Controller</b><br> ↳ <b>A-DS-DCShadow</b>: Possible DCShadow attack by asset detected.<br> ↳ <b>DS-DCSh-Add</b>: Directory service server object added<br> ↳ <b>DS-DCSh-Del</b>: Directory service server object created and deleted<br><br><b>T1558 - Steal or Forge Kerberos Tickets</b><br> ↳ <b>ATP-AS-REP-2</b>: Suspicious UAC directory service change indicating AS-REP Roasting<br><br><b>T1003.006 - OS Credential Dumping: DCSync</b><br> ↳ <b>A-DCSync</b>: Possible DCSync Attack: New domain controller detected<br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host. |  • <b>DS-HOSTS</b>: Models hosts in an Active Directory environment |
| failed-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-07</b>: Failed logon to an asset that user has not previously accessed    |  • <b>AE-UA</b>: All activity for users    |