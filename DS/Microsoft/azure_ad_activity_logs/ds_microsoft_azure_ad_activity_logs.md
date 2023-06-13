Vendor: Microsoft
=================
Product: Azure AD Activity Logs
-------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  87   |   41   |         12         |       6        |    6    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-password-change<br> ↳[microsoft-azuread-cef-user-password-modify-success-changeuserpassword](Ps/pC_microsoftazureadcefuserpasswordmodifysuccesschangeuserpassword.md)<br> ↳[microsoft-azuread-json-user-password-modify-success-passwordreset](Ps/pC_microsoftazureadjsonuserpasswordmodifysuccesspasswordreset.md)<br><br> app-activity<br> ↳[microsoft-m365auditlogs-json-app-activity-operationname](Ps/pC_microsoftm365auditlogsjsonappactivityoperationname.md)<br> ↳[microsoft-m365auditlogs-json-app-activity-appactivity](Ps/pC_microsoftm365auditlogsjsonappactivityappactivity.md)<br> ↳[microsoft-m365auditlogs-sk4-app-activity-graphdirectoryauditlogs](Ps/pC_microsoftm365auditlogssk4appactivitygraphdirectoryauditlogs.md)<br> ↳[microsoft-azure-json-app-activity-updategroup](Ps/pC_microsoftazurejsonappactivityupdategroup.md)<br> ↳[microsoft-azure-kv-app-activity-harddeletegroup](Ps/pC_microsoftazurekvappactivityharddeletegroup.md)<br> ↳[microsoft-azure-kv-app-activity-changeuserlicense](Ps/pC_microsoftazurekvappactivitychangeuserlicense.md)<br> ↳[microsoft-azure-json-app-activity-deletegroup](Ps/pC_microsoftazurejsonappactivitydeletegroup.md)<br> ↳[microsoft-azure-kv-app-activity-deleteuser](Ps/pC_microsoftazurekvappactivitydeleteuser.md)<br> ↳[microsoft-azure-json-app-activity-updateuser](Ps/pC_microsoftazurejsonappactivityupdateuser.md)<br> ↳[microsoft-azure-kv-app-activity-adduser](Ps/pC_microsoftazurekvappactivityadduser.md)<br> ↳[microsoft-azure-json-app-activity-groupmanagement](Ps/pC_microsoftazurejsonappactivitygroupmanagement.md)<br> ↳[microsoft-azure-json-app-activity-updatedevice](Ps/pC_microsoftazurejsonappactivityupdatedevice.md)<br> ↳[microsoft-azure-json-app-activity-addgroup](Ps/pC_microsoftazurejsonappactivityaddgroup.md)<br> ↳[microsoft-azuread-json-app-activity-addmembertogroup](Ps/pC_microsoftazureadjsonappactivityaddmembertogroup.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-containermanagedcluster](Ps/pC_microsoftazureadsk4appactivitysuccesscontainermanagedcluster.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-createupdate](Ps/pC_microsoftazureadsk4appactivitysuccesscreateupdate.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-provisionactivity](Ps/pC_microsoftazureadsk4appactivitysuccessprovisionactivity.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-other](Ps/pC_microsoftazureadsk4appactivitysuccessother.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-keyunwrap](Ps/pC_microsoftazureadsk4appactivitysuccesskeyunwrap.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-createupdateloadbalancer](Ps/pC_microsoftazureadsk4appactivitysuccesscreateupdateloadbalancer.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-import](Ps/pC_microsoftazureadsk4appactivitysuccessimport.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_microsoft_azure_ad_activity_logs_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  account-password-change<br> ↳[microsoft-azuread-cef-user-password-modify-success-changeuserpassword](Ps/pC_microsoftazureadcefuserpasswordmodifysuccesschangeuserpassword.md)<br> ↳[microsoft-azuread-json-user-password-modify-success-passwordreset](Ps/pC_microsoftazureadjsonuserpasswordmodifysuccesspasswordreset.md)<br><br> app-activity<br> ↳[microsoft-m365auditlogs-json-app-activity-operationname](Ps/pC_microsoftm365auditlogsjsonappactivityoperationname.md)<br> ↳[microsoft-m365auditlogs-json-app-activity-appactivity](Ps/pC_microsoftm365auditlogsjsonappactivityappactivity.md)<br> ↳[microsoft-m365auditlogs-sk4-app-activity-graphdirectoryauditlogs](Ps/pC_microsoftm365auditlogssk4appactivitygraphdirectoryauditlogs.md)<br> ↳[microsoft-azure-json-app-activity-updategroup](Ps/pC_microsoftazurejsonappactivityupdategroup.md)<br> ↳[microsoft-azure-kv-app-activity-harddeletegroup](Ps/pC_microsoftazurekvappactivityharddeletegroup.md)<br> ↳[microsoft-azure-kv-app-activity-changeuserlicense](Ps/pC_microsoftazurekvappactivitychangeuserlicense.md)<br> ↳[microsoft-azure-json-app-activity-deletegroup](Ps/pC_microsoftazurejsonappactivitydeletegroup.md)<br> ↳[microsoft-azure-kv-app-activity-deleteuser](Ps/pC_microsoftazurekvappactivitydeleteuser.md)<br> ↳[microsoft-azure-json-app-activity-updateuser](Ps/pC_microsoftazurejsonappactivityupdateuser.md)<br> ↳[microsoft-azure-kv-app-activity-adduser](Ps/pC_microsoftazurekvappactivityadduser.md)<br> ↳[microsoft-azure-json-app-activity-groupmanagement](Ps/pC_microsoftazurejsonappactivitygroupmanagement.md)<br> ↳[microsoft-azure-json-app-activity-updatedevice](Ps/pC_microsoftazurejsonappactivityupdatedevice.md)<br> ↳[microsoft-azure-json-app-activity-addgroup](Ps/pC_microsoftazurejsonappactivityaddgroup.md)<br> ↳[microsoft-azuread-json-app-activity-addmembertogroup](Ps/pC_microsoftazureadjsonappactivityaddmembertogroup.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-containermanagedcluster](Ps/pC_microsoftazureadsk4appactivitysuccesscontainermanagedcluster.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-createupdate](Ps/pC_microsoftazureadsk4appactivitysuccesscreateupdate.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-provisionactivity](Ps/pC_microsoftazureadsk4appactivitysuccessprovisionactivity.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-other](Ps/pC_microsoftazureadsk4appactivitysuccessother.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-keyunwrap](Ps/pC_microsoftazureadsk4appactivitysuccesskeyunwrap.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-createupdateloadbalancer](Ps/pC_microsoftazureadsk4appactivitysuccesscreateupdateloadbalancer.md)<br> ↳[microsoft-azuread-sk4-app-activity-success-import](Ps/pC_microsoftazureadsk4appactivitysuccessimport.md)<br> | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>4 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_microsoft_azure_ad_activity_logs_Account_Manipulation.md)    |
[Next Page -->>](2_ds_microsoft_azure_ad_activity_logs.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                                                                                                          | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                                                                                                          | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                                                                                                                   | Command and Control                                                                                                                                                                                                                                                                                                                                                                                      | Exfiltration | Impact |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Valid Accounts: Cloud Accounts](https://attack.mitre.org/techniques/T1078/004)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Unused/Unsupported Cloud Regions](https://attack.mitre.org/techniques/T1535)<br><br> |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br>[Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |