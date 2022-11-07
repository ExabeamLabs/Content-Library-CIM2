Vendor: Microsoft
=================
### Product: [ Event Viewer - Security](../ds_microsoft__event_viewer_-_security.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   2    |     1      |       1        |    1    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| service-created | <b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WSC-GH-F</b>: First service installation on host in the peer group<br> ↳ <b>WSC-GS-A</b>: Unusual service name in the peer group |  • <b>WSC-GS</b>: Services that are installed in the peer group<br> • <b>WSC-GH</b>: Hosts on which a new service is installed in the peer group |