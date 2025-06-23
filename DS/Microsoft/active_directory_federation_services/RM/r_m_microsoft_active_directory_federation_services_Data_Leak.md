Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Active Directory Federation Services](../ds_microsoft_active_directory_federation_services.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   2    |         5          |       1        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| web-activity-allowed | <b>T1041 - Exfiltration Over C2 Channel</b><br> ↳ <b>A-WEB-EXFIL-ASSET</b>: Large amount of data exfiltrated from host<br><br><b>T1567 - Exfiltration Over Web Service</b><br> ↳ <b>WEB-FS</b>: User has accessed a file sharing domain<br> ↳ <b>WEB-OU-FS</b>: One of the top file sharing users in the organization<br> ↳ <b>WEB-OG-FS</b>: One of the top file sharing users in the peer group<br> ↳ <b>A-WEB-EXFIL-ASSET</b>: Large amount of data exfiltrated from host<br><br><b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-New-File-20</b>: User has uploaded 20MB or more to an infrequently accessed top domain<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-New-File-20</b>: User has uploaded 20MB or more to an infrequently accessed top domain<br><br><b>T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage</b><br> ↳ <b>WEB-FS</b>: User has accessed a file sharing domain<br> ↳ <b>WEB-OU-FS</b>: One of the top file sharing users in the organization<br> ↳ <b>WEB-OG-FS</b>: One of the top file sharing users in the peer group |  • <b>WEB-OG-FS</b>: File sharing activities of users in the peer group<br> • <b>WEB-OU-FS</b>: File sharing activities of users in the organization |