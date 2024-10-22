|    Use-Case    | Activity Type (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br>    | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>28 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_liquidfiles_liquidfiles_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>6 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_liquidfiles_liquidfiles_Data_Access.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> endpoint-login:fail (authentication-failed)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br>    | T1078 - Valid Accounts<br>T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_liquidfiles_liquidfiles_Lateral_Movement.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  user-delete:success (account-deleted)<br> ↳[liquidfiles-l-json-user-deleted-success-inactiveuser](Ps/pC_liquidfilesljsonuserdeletedsuccessinactiveuser.md)<br><br> user-password-reset:success (account-password-reset)<br> ↳[liquidfiles-l-json-user-password-reset-success-password](Ps/pC_liquidfilesljsonuserpasswordresetsuccesspassword.md)<br><br> app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br><br> file-download:success (file-download)<br> ↳[liquidfiles-l-json-file-download-success-downloadsuccess](Ps/pC_liquidfilesljsonfiledownloadsuccessdownloadsuccess.md)<br> ↳[liquidfiles-l-json-file-download-success-downloading](Ps/pC_liquidfilesljsonfiledownloadsuccessdownloading.md)<br><br> file-upload:success (file-upload)<br> ↳[liquidfiles-l-json-file-upload-success-binaryuploadcomplete](Ps/pC_liquidfilesljsonfileuploadsuccessbinaryuploadcomplete.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br> | T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>T1531 - Account Access Removal<br>    | [<ul><li>5 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_liquidfiles_liquidfiles_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br><br> file-download:success (file-download)<br> ↳[liquidfiles-l-json-file-download-success-downloadsuccess](Ps/pC_liquidfilesljsonfiledownloadsuccessdownloadsuccess.md)<br> ↳[liquidfiles-l-json-file-download-success-downloading](Ps/pC_liquidfilesljsonfiledownloadsuccessdownloading.md)<br><br> file-upload:success (file-upload)<br> ↳[liquidfiles-l-json-file-upload-success-binaryuploadcomplete](Ps/pC_liquidfilesljsonfileuploadsuccessbinaryuploadcomplete.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_liquidfiles_liquidfiles_Privileged_Activity.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  app-login:success (app-login)<br> ↳[liquidfiles-l-json-app-login-success-ldapauthentication](Ps/pC_liquidfilesljsonapploginsuccessldapauthentication.md)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> endpoint-login:fail (authentication-failed)<br> ↳[liquidfiles-l-json-app-authentication-success-user](Ps/pC_liquidfilesljsonappauthenticationsuccessuser.md)<br><br> app-login:fail (failed-app-login)<br> ↳[liquidfiles-l-json-app-login-fail-ldapauthenticationerror](Ps/pC_liquidfilesljsonapploginfailldapauthenticationerror.md)<br> ↳[liquidfiles-l-json-file-upload-success-message](Ps/pC_liquidfilesljsonfileuploadsuccessmessage.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_liquidfiles_liquidfiles_Ransomware.md)    |