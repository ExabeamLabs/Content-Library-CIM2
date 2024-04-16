Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft Exchange](../ds_microsoft_microsoft_exchange.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  15   |   2    |         7          |       8        |    7    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity          | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |    |
| app-activity-failed   | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| app-login    | <b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost</b>: User authentication or login from a known TOR IP    |    |
| authentication-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| failed-app-login      | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP    |    |
| nac-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user<br> ↳ <b>NAC-UM-F</b>: First MAC for user<br> ↳ <b>NAC-UM-A</b>: Abnormal MAC for user<br><br><b>T1021 - Remote Services</b><br> ↳ <b>NAC-UL-F</b>: First network location for user<br> ↳ <b>NAC-UL-A</b>: Abnormal network location for user    |  • <b>NAC-UM</b>: MAC addresses for user<br> • <b>NAC-UL</b>: Network locations for user |
| security-alert        | <b>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools</b><br> ↳ <b>A-ALERT-DL</b>: DL Correlation rule alert on asset    |    |
| web-activity-allowed  | <b>T1190 - Exploit Public Fasing Application</b><br> ↳ <b>A-NET-Log4j-IP</b>: Asset was accessed by an external IP associated with Log4j exploit<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>WEB-UD-TorProxy</b>: User has accessed a known Tor web proxy<br> ↳ <b>WEB-UI-Tor</b>: User has accessed a known Tor exit node<br> ↳ <b>WEB-URank-Tor</b>: User has accessed a tor-to-web proxy site<br> ↳ <b>A-WEB-TorProxy</b>: Asset has accessed a known Tor web proxy<br> ↳ <b>A-WEB-UU-Tor</b>: Asset has accessed a URL containing '/tor/server'<br> ↳ <b>A-NET-TOR-Outbound</b>: Outbound connection to a known TOR IP<br><br><b>TA0011 - TA0011</b><br> ↳ <b>A-NET-TI-IP-Outbound</b>: Outbound connection to a known malicious IP<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-URank-Tor</b>: User has accessed a tor-to-web proxy site |    |