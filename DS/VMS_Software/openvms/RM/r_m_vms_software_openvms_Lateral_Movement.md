Rules by Product and UseCase
============================
Vendor: VMS Software
--------------------
### Product: [OpenVMS](../ds_vms_software_openvms.md)
### Use-Case: [Lateral Movement](../../../../UseCases/uc_lateral_movement.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   1    |         7          |       1        |    1    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon | <b>T1550.002 - Use Alternate Authentication Material: Pass the Hash</b><br> ↳ <b>FAIL-PTH-ALERT-sH</b>: Possible unsuccessful pass the hash attack from the source<br> ↳ <b>FAIL-PTH-ALERT-dH</b>: Possible unsuccessful pass the hash attack by the user<br> ↳ <b>PTH-ALERT-sH-Failed</b>: Failed pass the hash attack with keylength of 0 in NTLM event and a 'null' sid.<br><br><b>T1021.001 - Remote Services: Remote Desktop Protocol</b><br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user<br><br><b>T1110 - Brute Force</b><br> ↳ <b>RDP-Brute-Force</b>: Abnormal number of RDP failed logons for this user<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1090.003 - Proxy: Multi-hop Proxy</b><br> ↳ <b>Auth-Tor-Shost-Failed</b>: User authentication or login failure from a known TOR IP<br><br><b>T1550.003 - Use Alternate Authentication Material: Pass the Ticket</b><br> ↳ <b>KL-TfG</b>: Rare Kerberos ticket failure code<br> ↳ <b>KL-Tf-fail</b>: Failed logon due to a malformed authentication ticket<br><br><b>T1558 - Steal or Forge Kerberos Tickets</b><br> ↳ <b>KL-TfG</b>: Rare Kerberos ticket failure code<br> ↳ <b>KL-Tf-fail</b>: Failed logon due to a malformed authentication ticket |  • <b>AE-OHr</b>: Random hostnames |