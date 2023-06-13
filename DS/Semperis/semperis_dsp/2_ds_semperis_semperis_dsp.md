|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> ds-access<br> ↳[semperis-dsp-str-ds-object-create-success-createobject](Ps/pC_semperisdspstrdsobjectcreatesuccesscreateobject.md)<br> ↳[semperis-dsp-str-ds-object-delete-success-deleteobject](Ps/pC_semperisdspstrdsobjectdeletesuccessdeleteobject.md)<br> ↳[semperis-dsp-str-ds-object-modify-success-modifyobject](Ps/pC_semperisdspstrdsobjectmodifysuccessmodifyobject.md)<br> ↳[semperis-dsp-str-ds-object-move-success-moveobject](Ps/pC_semperisdspstrdsobjectmovesuccessmoveobject.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> | T1003.006 - OS Credential Dumping: DCSync<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br>T1207 - Rogue Domain Controller<br>T1558 - Steal or Forge Kerberos Tickets<br> | [<ul><li>50 Rules</li></ul><ul><li>25 Models</li></ul>](RM/r_m_semperis_semperis_dsp_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>20 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_semperis_semperis_dsp_Data_Access.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br>    | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_semperis_semperis_dsp_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> privileged-object-access<br> ↳[semperis-dsp-kv-user-privilege-use-success-permissionchanges](Ps/pC_semperisdspkvuserprivilegeusesuccesspermissionchanges.md)<br>    | T1078 - Valid Accounts<br>TA0002 - TA0002<br>    | [<ul><li>5 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_semperis_semperis_dsp_Malware.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> ds-access<br> ↳[semperis-dsp-str-ds-object-create-success-createobject](Ps/pC_semperisdspstrdsobjectcreatesuccesscreateobject.md)<br> ↳[semperis-dsp-str-ds-object-delete-success-deleteobject](Ps/pC_semperisdspstrdsobjectdeletesuccessdeleteobject.md)<br> ↳[semperis-dsp-str-ds-object-modify-success-modifyobject](Ps/pC_semperisdspstrdsobjectmodifysuccessmodifyobject.md)<br> ↳[semperis-dsp-str-ds-object-move-success-moveobject](Ps/pC_semperisdspstrdsobjectmovesuccessmoveobject.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> | T1078 - Valid Accounts<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>T1484 - Group Policy Modification<br>    | [<ul><li>8 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_semperis_semperis_dsp_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> ds-access<br> ↳[semperis-dsp-str-ds-object-create-success-createobject](Ps/pC_semperisdspstrdsobjectcreatesuccesscreateobject.md)<br> ↳[semperis-dsp-str-ds-object-delete-success-deleteobject](Ps/pC_semperisdspstrdsobjectdeletesuccessdeleteobject.md)<br> ↳[semperis-dsp-str-ds-object-modify-success-modifyobject](Ps/pC_semperisdspstrdsobjectmodifysuccessmodifyobject.md)<br> ↳[semperis-dsp-str-ds-object-move-success-moveobject](Ps/pC_semperisdspstrdsobjectmovesuccessmoveobject.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> | T1003.006 - OS Credential Dumping: DCSync<br>T1078 - Valid Accounts<br>T1207 - Rogue Domain Controller<br>T1484 - Group Policy Modification<br>    | [<ul><li>9 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_semperis_semperis_dsp_Privileged_Activity.md)       |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  app-activity<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfound](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfound.md)<br> ↳[semperis-dsp-kv-endpoint-notification-success-indicatorfailed](Ps/pC_semperisdspkvendpointnotificationsuccessindicatorfailed.md)<br><br> app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br> ↳[semperis-dsp-str-app-login-success-logindsp](Ps/pC_semperisdspstrapploginsuccesslogindsp.md)<br><br> failed-app-login<br> ↳[semperis-dsp-kv-app-login-logintodsp](Ps/pC_semperisdspkvapploginlogintodsp.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_semperis_semperis_dsp_Ransomware.md)    |