Rules by Product and UseCase
============================
Vendor: Dropbox
---------------
### Product: [Dropbox](../ds_dropbox_dropbox.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         2          |       2        |   14    |

| Event Type | Rules    | Models |
| ---------- | ---- | ------ |
| app-login  | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |
| file-write | <b>T1486 - Data Encrypted for Impact</b><br> ↳ <b>FA-EXT</b>: A file has been written and is suspected of Ransomware on host |        |