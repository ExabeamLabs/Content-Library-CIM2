Vendor: Microsoft
=================
Product: Azure MFA
------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   0   |   0    |     0      |       7        |    7    |

|  Use-Case  | Activity Types/Parsers    | MITRE TTP | Content    |
|:----------:| ---- | --------- | ---- |
| Enrichment |  ""process-token-modify:success""<br> ↳[microsoft-azuremfa-process-token-modify-pfsvc](Ps/pC_microsoftazuremfaprocesstokenmodifypfsvc.md)<br><br> ""user-modify:success""<br> ↳[microsoft-azuremfa-user-modify-deleted](Ps/pC_microsoftazuremfausermodifydeleted.md)<br> ↳[microsoft-azuremfa-str-user-modify-changed](Ps/pC_microsoftazuremfastrusermodifychanged.md)<br> ↳[microsoft-azuremfa-user-modify-added](Ps/pC_microsoftazuremfausermodifyadded.md)<br><br> "account-deleted"<br> ↳[microsoft-azuremfa-user-delete-deleted](Ps/pC_microsoftazuremfauserdeletedeleted.md)<br><br> "authentication-failed"<br> ↳[microsoft-azuremfa-str-app-authentication-fail-failed](Ps/pC_microsoftazuremfastrappauthenticationfailfailed.md)<br> ↳[microsoft-azuremfa-str-app-authentication-fail-from](Ps/pC_microsoftazuremfastrappauthenticationfailfrom.md)<br> ↳[microsoft-azuremfa-str-app-authentication-fail-validate-security-question-answers](Ps/pC_microsoftazuremfastrappauthenticationfailvalidatesecurityquestionanswers.md)<br><br> "authentication-successful"<br> ↳[microsoft-azuremfa-str-app-authentication-primery](Ps/pC_microsoftazuremfastrappauthenticationprimery.md)<br> ↳[microsoft-azuremfa-str-app-authentication-validate-oath-code-1](Ps/pC_microsoftazuremfastrappauthenticationvalidateoathcode1.md)<br> ↳[microsoft-azuremfa-str-app-authentication-validate-oath-code](Ps/pC_microsoftazuremfastrappauthenticationvalidateoathcode.md)<br><br> "computer-logon"<br> ↳[microsoft-azuremfa-str-endpoint-login-success-callstatus](Ps/pC_microsoftazuremfastrendpointloginsuccesscallstatus.md)<br><br> "nac-failed-logon"<br> ↳[microsoft-azuremfa-str-endpoint-login-fail-pfsvc](Ps/pC_microsoftazuremfastrendpointloginfailpfsvc.md)<br> |    | [](RM/r_m_microsoft_azure_mfa_Enrichment.md) |

ATT&CK Matrix for Enterprise
----------------------------
