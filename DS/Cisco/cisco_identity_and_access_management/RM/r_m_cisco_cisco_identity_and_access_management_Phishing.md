Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco Identity and Access Management](../ds_cisco_cisco_identity_and_access_management.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         2          |       2        |    2    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| process-created | <b>T1566 - Phishing</b><br> ↳ <b>A-Exec-Outlook-Temp</b>: A suspicious program was executed in the Outlook temp folder on this asset.<br><br><b>T1566.001 - T1566.001</b><br> ↳ <b>A-Exec-Outlook-Temp</b>: A suspicious program was executed in the Outlook temp folder on this asset. |    |
| vpn-logout      | <b>T1566 - Phishing</b><br> ↳ <b>EM-FNum-in</b>: Abnormal number of incoming emails<br> ↳ <b>EM-BSum-in</b>: Abnormal size of incoming emails    |  • <b>EM-BSum-in</b>: Sum of bytes in incoming emails<br> • <b>EM-FNum-in</b>: Count of incoming emails |