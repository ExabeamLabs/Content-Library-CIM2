Vendor: Google
==============
Product: Google Cloud Platform
------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  291  |  142   |         44         |       26       |   26    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-creation<br> ↳[google-cloudplatform-json-user-create-success-googleiamcreateserviceaccount](Ps/pC_googlecloudplatformjsonusercreatesuccessgoogleiamcreateserviceaccount.md)<br><br> app-activity<br> ↳[google-cloudplatform-mix-app-activity-success-prototpayload](Ps/pC_googlecloudplatformmixappactivitysuccessprototpayload.md)<br> ↳[google-cloudplatform-json-app-database-success-database](Ps/pC_googlecloudplatformjsonappdatabasesuccessdatabase.md)<br> ↳[google-cloudplatform-json-scheduled-success-scheduler](Ps/pC_googlecloudplatformjsonscheduledsuccessscheduler.md)<br> ↳[google-cloudplatform-json-scheduled-success-scheduler](Ps/pC_googlecloudplatformjsonscheduledsuccessscheduler.md)<br> ↳[google-cloudplatform-json-app-activity-success-googleapismethodname](Ps/pC_googlecloudplatformjsonappactivitysuccessgoogleapismethodname.md)<br><br> web-activity-allowed<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br><br> web-activity-denied<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_google_google_cloud_platform_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  account-creation<br> ↳[google-cloudplatform-json-user-create-success-googleiamcreateserviceaccount](Ps/pC_googlecloudplatformjsonusercreatesuccessgoogleiamcreateserviceaccount.md)<br><br> app-activity<br> ↳[google-cloudplatform-mix-app-activity-success-prototpayload](Ps/pC_googlecloudplatformmixappactivitysuccessprototpayload.md)<br> ↳[google-cloudplatform-json-app-database-success-database](Ps/pC_googlecloudplatformjsonappdatabasesuccessdatabase.md)<br> ↳[google-cloudplatform-json-scheduled-success-scheduler](Ps/pC_googlecloudplatformjsonscheduledsuccessscheduler.md)<br> ↳[google-cloudplatform-json-scheduled-success-scheduler](Ps/pC_googlecloudplatformjsonscheduledsuccessscheduler.md)<br> ↳[google-cloudplatform-json-app-activity-success-googleapismethodname](Ps/pC_googlecloudplatformjsonappactivitysuccessgoogleapismethodname.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>T1136 - Create Account<br>T1136.001 - Create Account: Create: Local Account<br>T1136.002 - T1136.002<br> | [<ul><li>23 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_google_google_cloud_platform_Account_Manipulation.md)    |
|    [Cryptomining](../../../UseCases/uc_cryptomining.md)    |  gcp-instance-create<br> ↳[google-cloudplatform-json-endpoint-create-success-betacomputeinstancesinsert](Ps/pC_googlecloudplatformjsonendpointcreatesuccessbetacomputeinstancesinsert.md)<br><br> web-activity-allowed<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br><br> web-activity-denied<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br>    | T1071.001 - Application Layer Protocol: Web Protocols<br>T1074 - Data Staged<br>T1496 - Resource Hijacking<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_google_google_cloud_platform_Cryptomining.md)    |
|    [Phishing](../../../UseCases/uc_phishing.md)    |  web-activity-allowed<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br><br> web-activity-denied<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br>    | T1189 - Drive-by Compromise<br>T1204.001 - T1204.001<br>T1534 - Internal Spearphishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1598.003 - T1598.003<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_google_google_cloud_platform_Phishing.md)    |
|    [Workforce Protection](../../../UseCases/uc_workforce_protection.md)    |  web-activity-allowed<br> ↳[google-cloudplatform-json-http-session-httploadbalancer](Ps/pC_googlecloudplatformjsonhttpsessionhttploadbalancer.md)<br>    | T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_google_google_cloud_platform_Workforce_Protection.md)    |
[Next Page -->>](2_ds_google_google_cloud_platform.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Execution                                                           | Persistence                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Privilege Escalation                                                                                                                                      | Defense Evasion                                                                                                                                          | Credential Access                                                          | Discovery                                                                         | Lateral Movement                                                            | Collection                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Command and Control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Exfiltration                                                                                                                                                                                                                                                                                                                                                        | Impact                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Phishing: Spearphishing Link](https://attack.mitre.org/techniques/T1566/002)<br><br>[External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Drive-by Compromise](https://attack.mitre.org/techniques/T1189)<br><br>[Valid Accounts: Cloud Accounts](https://attack.mitre.org/techniques/T1078/004)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br>[Phishing](https://attack.mitre.org/techniques/T1566)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [Create Account](https://attack.mitre.org/techniques/T1136)<br><br>[External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Server Software Component: Web Shell](https://attack.mitre.org/techniques/T1505/003)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Server Software Component](https://attack.mitre.org/techniques/T1505)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br>[Create Account: Create: Local Account](https://attack.mitre.org/techniques/T1136/001)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Unused/Unsupported Cloud Regions](https://attack.mitre.org/techniques/T1535)<br><br> | [OS Credential Dumping](https://attack.mitre.org/techniques/T1003)<br><br> | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> | [Internal Spearphishing](https://attack.mitre.org/techniques/T1534)<br><br> | [Screen Capture](https://attack.mitre.org/techniques/T1113)<br><br>[Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br>[Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530)<br><br>[Data Staged](https://attack.mitre.org/techniques/T1074)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Web Service](https://attack.mitre.org/techniques/T1102)<br><br>[Application Layer Protocol: Web Protocols](https://attack.mitre.org/techniques/T1071/001)<br><br>[Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over C2 Channel](https://attack.mitre.org/techniques/T1041)<br><br>[Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br>[Exfiltration Over Web Service: Exfiltration to Cloud Storage](https://attack.mitre.org/techniques/T1567/002)<br><br>[Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567)<br><br> | [Resource Hijacking](https://attack.mitre.org/techniques/T1496)<br><br>[Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486)<br><br> |