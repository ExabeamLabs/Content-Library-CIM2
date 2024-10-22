Rules by Product and UseCase
============================
Vendor: Oracle
--------------
### Product: [Solaris](../ds_oracle_solaris.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         12         |       1        |    0    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1059 - Command and Scripting Interperter</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1059.003 - T1059.003</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1222 - File and Directory Permissions Modification</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1222.001 - File and Directory Permissions Modification: Windows File and Directory Permissions Modification</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1490 - Inhibit System Recovery</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1070 - Indicator Removal on Host</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br> ↳ <b>A-Fsutil-Sus-Invocation</b>: Suspicious parameters of fsutil were detected on this asset.<br><br><b>T1003 - OS Credential Dumping</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1003.001 - T1003.001</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1218 - Signed Binary Proxy Execution</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1218.011 - Signed Binary Proxy Execution: Rundll32</b><br> ↳ <b>A-NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset |        |