#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-644"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="644""""
]
Fields = [
"""EventID=\"+({event_code}[^\"]+)\""""
"""EventRecordID=\"+({event_id}[^\"]+)\""""
"""CallerDomain=\"+({domain}({src_domain}[^\"]+))\""""
"""CallerLogonId=\"+\([^,]+,({login_id}[^\)]+)\""""
"""CallerUserName =\"+({src_user}[^\"]+)\""""
"""TargetAccountID=\"+\%\{({user_sid}[^}]+)\}\""""
"""TargetAccountName =\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""CallerMachineName =\"+({src_host}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```