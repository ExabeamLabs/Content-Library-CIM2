|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
|         [Cryptomining](../../../UseCases/uc_cryptomining.md)         |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1496 - Resource Hijacking<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Cryptomining.md)    |
|          [Data Access](../../../UseCases/uc_data_access.md)          |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1083 - File and Directory Discovery<br>    | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_vectra_cognito_stream_Data_Access.md)        |
|    [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)    |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1041 - Exfiltration Over C2 Channel<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1567 - Exfiltration Over Web Service<br>T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>TA0002 - TA0002<br>    | [<ul><li>10 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_vectra_cognito_stream_Data_Exfiltration.md)   |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1041 - Exfiltration Over C2 Channel<br>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1114.001 - T1114.001<br>T1567 - Exfiltration Over Web Service<br>T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage<br>    | [<ul><li>39 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_vectra_cognito_stream_Data_Leak.md)          |
|  [Destruction of Data](../../../UseCases/uc_destruction_of_data.md)  |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1070.004 - Indicator Removal on Host: File Deletion<br>T1485 - Data Destruction<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Destruction_of_Data.md)    |
|     [Lateral Movement](../../../UseCases/uc_lateral_movement.md)     |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>    | [<ul><li>11 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1003.002 - T1003.002<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1189 - Drive-by Compromise<br>T1190 - Exploit Public Fasing Application<br>T1204.001 - T1204.001<br>T1505.003 - Server Software Component: Web Shell<br>T1547.001 - T1547.001<br>T1566.002 - Phishing: Spearphishing Link<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>TA0002 - TA0002<br> | [<ul><li>37 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_vectra_cognito_stream_Malware.md)    |
|    [Phishing](../../../UseCases/uc_phishing.md)    |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br>T1189 - Drive-by Compromise<br>T1204.001 - T1204.001<br>T1534 - Internal Spearphishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1598.003 - T1598.003<br>    | [<ul><li>5 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_vectra_cognito_stream_Phishing.md)    |
|      [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)      |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Privilege_Abuse.md)    |
|  [Privileged Activity](../../../UseCases/uc_privileged_activity.md)  |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1102 - Web Service<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Privileged_Activity.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1486 - Data Encrypted for Impact<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_vectra_cognito_stream_Ransomware.md)    |
| [Workforce Protection](../../../UseCases/uc_workforce_protection.md) |  authentication-failed<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> authentication-successful<br> ↳[vectra-cs-kv-app-authentication-success-resultcode](Ps/pC_vectracskvappauthenticationsuccessresultcode.md)<br><br> computer-logon<br> ↳[vectra-cs-kv-endpoint-login-success-metadatantlm](Ps/pC_vectracskvendpointloginsuccessmetadatantlm.md)<br><br> dlp-email-alert-out<br> ↳[vectra-cs-kv-email-send-success-metadatasmtp](Ps/pC_vectracskvemailsendsuccessmetadatasmtp.md)<br><br> file-delete<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-read<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> file-write<br> ↳[vectra-cs-kv-file-write-success-metadatasmbfiles](Ps/pC_vectracskvfilewritesuccessmetadatasmbfiles.md)<br><br> web-activity-allowed<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br><br> web-activity-denied<br> ↳[vectra-cs-kv-http-session-httpsessioninfo](Ps/pC_vectracskvhttpsessionhttpsessioninfo.md)<br> | T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>8 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_vectra_cognito_stream_Workforce_Protection.md) |