Vendor: Microsoft
=================
Product: Active Directory Federation Services
---------------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  65   |   26   |     6      |       6        |    6    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-notification:success""<br> ↳[microsoft-adfs-cef-app-notification-success-431](Ps/pC_microsoftadfscefappnotificationsuccess431.md)<br> ↳[microsoft-adfs-cef-app-notification-success-410](Ps/pC_microsoftadfscefappnotificationsuccess410.md)<br> ↳[microsoft-adfs-str-app-notification-success-501](Ps/pC_microsoftadfsstrappnotificationsuccess501.md)<br><br> ""http-response:success""<br> ↳[microsoft-adfs-cef-http-response-success-404](Ps/pC_microsoftadfscefhttpresponsesuccess404.md)<br> ↳[microsoft-adfs-kv-http-response-success-dispatched](Ps/pC_microsoftadfskvhttpresponsesuccessdispatched.md)<br><br> account-lockout<br> ↳[microsoft-adfs-kv-user-lock-success-512](Ps/pC_microsoftadfskvuserlocksuccess512.md)<br> ↳[microsoft-adfs-kv-user-lock-success-516](Ps/pC_microsoftadfskvuserlocksuccess516.md)<br><br> app-activity<br> ↳[microsoft-adfs-cef-http-request-success-1102](Ps/pC_microsoftadfscefhttprequestsuccess1102.md)<br> ↳[microsoft-adfs-cef-http-request-success-403](Ps/pC_microsoftadfscefhttprequestsuccess403.md)<br> ↳[microsoft-adfs-kv-http-request-audit](Ps/pC_microsoftadfskvhttprequestaudit.md)<br><br> authentication-failed<br> ↳[microsoft-adfs-kv-app-authentication-fail-413](Ps/pC_microsoftadfskvappauthenticationfail413.md)<br> ↳[microsoft-adfs-kv-app-authentication-fail-324](Ps/pC_microsoftadfskvappauthenticationfail324.md)<br> ↳[microsoft-adfs-cef-app-authentication-fail-324](Ps/pC_microsoftadfscefappauthenticationfail324.md)<br> ↳[microsoft-adfs-kv-app-authentication-fail-411](Ps/pC_microsoftadfskvappauthenticationfail411.md)<br><br> authentication-successful<br> ↳[microsoft-adfs-cef-app-authentication-success-412](Ps/pC_microsoftadfscefappauthenticationsuccess412.md)<br> | T1078 - Valid Accounts<br>T1110 - Brute Force<br>T1133 - External Remote Services<br> | [<ul><li>16 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_microsoft_active_directory_federation_services_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-notification:success""<br> ↳[microsoft-adfs-cef-app-notification-success-431](Ps/pC_microsoftadfscefappnotificationsuccess431.md)<br> ↳[microsoft-adfs-cef-app-notification-success-410](Ps/pC_microsoftadfscefappnotificationsuccess410.md)<br> ↳[microsoft-adfs-str-app-notification-success-501](Ps/pC_microsoftadfsstrappnotificationsuccess501.md)<br><br> ""http-response:success""<br> ↳[microsoft-adfs-cef-http-response-success-404](Ps/pC_microsoftadfscefhttpresponsesuccess404.md)<br> ↳[microsoft-adfs-kv-http-response-success-dispatched](Ps/pC_microsoftadfskvhttpresponsesuccessdispatched.md)<br><br> account-lockout<br> ↳[microsoft-adfs-kv-user-lock-success-512](Ps/pC_microsoftadfskvuserlocksuccess512.md)<br> ↳[microsoft-adfs-kv-user-lock-success-516](Ps/pC_microsoftadfskvuserlocksuccess516.md)<br><br> app-activity<br> ↳[microsoft-adfs-cef-http-request-success-1102](Ps/pC_microsoftadfscefhttprequestsuccess1102.md)<br> ↳[microsoft-adfs-cef-http-request-success-403](Ps/pC_microsoftadfscefhttprequestsuccess403.md)<br> ↳[microsoft-adfs-kv-http-request-audit](Ps/pC_microsoftadfskvhttprequestaudit.md)<br><br> authentication-failed<br> ↳[microsoft-adfs-kv-app-authentication-fail-413](Ps/pC_microsoftadfskvappauthenticationfail413.md)<br> ↳[microsoft-adfs-kv-app-authentication-fail-324](Ps/pC_microsoftadfskvappauthenticationfail324.md)<br> ↳[microsoft-adfs-cef-app-authentication-fail-324](Ps/pC_microsoftadfscefappauthenticationfail324.md)<br> ↳[microsoft-adfs-kv-app-authentication-fail-411](Ps/pC_microsoftadfskvappauthenticationfail411.md)<br><br> authentication-successful<br> ↳[microsoft-adfs-cef-app-authentication-success-412](Ps/pC_microsoftadfscefappauthenticationsuccess412.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_microsoft_active_directory_federation_services_Account_Manipulation.md)    |
[Next Page -->>](2_ds_microsoft_active_directory_federation_services.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br> |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |