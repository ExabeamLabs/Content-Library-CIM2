Rules by Product and UseCase
============================
Vendor: Check Point
-------------------
### Product: [Check Point Security Gateway](../ds_check_point_check_point_security_gateway.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   5    |         4          |       4        |   20    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| failed-vpn-login      | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| nac-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user<br> ↳ <b>NAC-UM-F</b>: First MAC for user<br> ↳ <b>NAC-UM-A</b>: Abnormal MAC for user<br><br><b>T1021 - Remote Services</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user    |  • <b>NAC-UM</b>: MAC addresses for user<br> • <b>NAC-UL</b>: Network locations for user    |
| vpn-login    | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |    |
| vpn-logout    | <b>T1558.003 - Steal or Forge Kerberos Tickets: Kerberoasting</b><br> ↳ <b>KL-USnCOUNT-A</b>: Abnormal number of services used to obtain TGTs by user<br> ↳ <b>KL-GSnCOUNT-A</b>: Abnormal number of services used to obtain TGTs by peer group<br><br><b>T1021 - Remote Services</b><br> ↳ <b>RA-UHcount-S</b>: Abnormal number of accessed hosts for user (S)<br> ↳ <b>RA-UHcount-M</b>: Abnormal number of accessed hosts for user (M)<br> ↳ <b>RA-UHcount-L</b>: Abnormal number of accessed hosts for user (L)<br> ↳ <b>RA-OHcount</b>: Abnormal number of accessed hosts for the organization<br> ↳ <b>RA-GHcount</b>: Abnormal number of accessed assets for group<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>RA-UHcount-S</b>: Abnormal number of accessed hosts for user (S)<br> ↳ <b>RA-UHcount-M</b>: Abnormal number of accessed hosts for user (M)<br> ↳ <b>RA-UHcount-L</b>: Abnormal number of accessed hosts for user (L)<br> ↳ <b>RA-OHcount</b>: Abnormal number of accessed hosts for the organization<br> ↳ <b>RA-GHcount</b>: Abnormal number of accessed assets for group |  • <b>KL-GSnCOUNT</b>: Count of services used to obtain kerberos TGTs in a session for peer group<br> • <b>KL-USnCOUNT</b>: Count of services used to obtain kerberos TGTs in a session for user<br> • <b>RA-OHcount</b>: Count of assets access per user in the organization |