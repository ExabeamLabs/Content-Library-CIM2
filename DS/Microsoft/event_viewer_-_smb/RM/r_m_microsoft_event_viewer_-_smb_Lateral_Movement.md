Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - SMB](../ds_microsoft_event_viewer_-_smb.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   9   |   4    |         4          |       2        |    4    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-successful | <b>T1090 - Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |    |
| share-access    | <b>T1021 - Remote Services</b><br> ↳ <b>A-SA-OU-F</b>: First admin share access to asset for this user in the organization<br> ↳ <b>A-SA-OU-A</b>: Abnormal admin share access to asset for the user in the organization<br> ↳ <b>A-SA-OH-F</b>: First admin share on asset for organization<br> ↳ <b>A-SA-OH-A</b>: Abnormal admin share on asset in organization<br> ↳ <b>A-SA-ZH-F</b>: First admin share on asset in the zone<br> ↳ <b>A-SA-ZH-A</b>: Abnormal admin share on asset for zone<br> ↳ <b>A-SA-AsU-F</b>: First access of admin share on asset<br> ↳ <b>A-SA-AsU-A</b>: Abnormal access of admin share on the asset<br><br><b>T1021.002 - Remote Services: SMB/Windows Admin Shares</b><br> ↳ <b>A-SA-OU-F</b>: First admin share access to asset for this user in the organization<br> ↳ <b>A-SA-OU-A</b>: Abnormal admin share access to asset for the user in the organization<br> ↳ <b>A-SA-OH-F</b>: First admin share on asset for organization<br> ↳ <b>A-SA-OH-A</b>: Abnormal admin share on asset in organization<br> ↳ <b>A-SA-ZH-F</b>: First admin share on asset in the zone<br> ↳ <b>A-SA-ZH-A</b>: Abnormal admin share on asset for zone<br> ↳ <b>A-SA-AsU-F</b>: First access of admin share on asset<br> ↳ <b>A-SA-AsU-A</b>: Abnormal access of admin share on the asset |  • <b>A-SA-AsU</b>: Users per Admin share<br> • <b>A-SA-ZH</b>: Dest zones on which admin shares are accessed<br> • <b>A-SA-OH</b>: Assets on which admin shares are accessed in organization<br> • <b>A-SA-OU</b>: Admin Share users in organization |