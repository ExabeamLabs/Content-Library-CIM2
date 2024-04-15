Rules by Product and UseCase
============================
Vendor: Tanium
--------------
### Product: [Tanium Integrity Monitor](../ds_tanium_tanium_integrity_monitor.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   0    |         9          |       4        |    4    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| file-write    | <b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>FA-EXT</b>: A file has been written and is suspected of Ransomware on host    |        |
| network-connection-failed     | <b>TA0011 - TA0011</b><br> ↳ <b>A-NETF-Ransomware-IP</b>: Asset failed to connect to an IP address which is associated to Ransomware    |        |
| network-connection-successful | <b>TA0011 - TA0011</b><br> ↳ <b>A-NET-Ransomware-IP</b>: Asset attempted to connect to an IP address which is associated to Ransomware    |        |
| process-created    | <b>T1059.003 - T1059.003</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1222.001 - File and Directory Permissions Modification: Windows File and Directory Permissions Modification</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1490 - Inhibit System Recovery</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1070 - Indicator Removal on Host</b><br> ↳ <b>A-Fsutil-Sus-Invocation</b>: Suspicious parameters of fsutil were detected on this asset.<br><br><b>T1003.001 - T1003.001</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1218.011 - Signed Binary Proxy Execution: Rundll32</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset |        |