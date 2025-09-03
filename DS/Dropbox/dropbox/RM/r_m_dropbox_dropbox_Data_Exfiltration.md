Rules by Product and UseCase
============================
Vendor: Dropbox
---------------
### Product: [Dropbox](../ds_dropbox_dropbox.md)
### Use-Case: [Data Exfiltration](../../../../UseCases/uc_data_exfiltration.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   5    |         3          |       2        |   10    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| file-write | <b>TA0002 - TA0002</b><br> ↳ <b>FA-TEMP-DIRECTORY-F</b>: First time process has been executed from a temporary directory by this user during file activity<br> ↳ <b>FA-TEMP-DIRECTORY-A</b>: Abnormal process has been executed from a temporary directory by this user during file activity    |  • <b>FA-UP-TEMP</b>: Process executable TEMP directories for this user during file activity    |
| vpn-logout | <b>T1133 - External Remote Services</b><br> ↳ <b>VPN-BSum</b>: Abnormal amount of data uploaded during VPN Session<br><br><b>TA0010 - TA0010</b><br> ↳ <b>DLP-UPCOUNT</b>: Abnormal number of DLP policy violations for user<br> ↳ <b>DLP-GPCOUNT</b>: Abnormal number of DLP policy violations for peer group<br> ↳ <b>DLP-BSum</b>: Abnormal amount of data written during DLP policy violation |  • <b>VPN-BSum</b>: Sum of bytes uploaded during VPN<br> • <b>DLP-BSum</b>: Sum of bytes written during DLP policy violation<br> • <b>DLP-GPCOUNT</b>: Count of DLP policy violations for peer group<br> • <b>DLP-UPCOUNT</b>: Count of DLP policy violations for user |