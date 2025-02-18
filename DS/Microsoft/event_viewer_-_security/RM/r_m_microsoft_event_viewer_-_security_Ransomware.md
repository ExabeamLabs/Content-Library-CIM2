Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   0    |         13         |       6        |   249   |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| authentication-failed     | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost-Failed</b>: User authentication or login failure from a known ransomware IP    |        |
| authentication-successful | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |
| failed-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost-Failed</b>: User authentication or login failure from a known ransomware IP    |        |
| file-write    | <b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>FA-EXT</b>: A file has been written and is suspected of Ransomware on host    |        |
| process-created    | <b>T1059 - Command and Scripting Interperter</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1059.003 - T1059.003</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1222 - File and Directory Permissions Modification</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1222.001 - File and Directory Permissions Modification: Windows File and Directory Permissions Modification</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1490 - Inhibit System Recovery</b><br> ↳ <b>A-WannaCry</b>: Artifacts seen by WannaCry malware have been observed on this asset<br><br><b>T1070 - Indicator Removal on Host</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br> ↳ <b>A-Fsutil-Sus-Invocation</b>: Suspicious parameters of fsutil were detected on this asset.<br><br><b>T1003 - OS Credential Dumping</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1003.001 - T1003.001</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1218 - Signed Binary Proxy Execution</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset<br><br><b>T1218.011 - Signed Binary Proxy Execution: Rundll32</b><br> ↳ <b>NotPetya-Activity</b>: NotPetya Ransomware Activity detected on this asset |        |
| remote-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |