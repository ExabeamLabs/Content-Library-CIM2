#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-modify-627-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="627""""
]
Fields = [
"""({event_name}Change Password Attempt)"""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""CallerDomain="+({domain}[^"]+)""""
"""CallerLogonId="+\([^,]+,({login_id}[^\)]+)""""
"""CallerUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""TargetAccountID="+\%\{({dest_user_sid}[^}]+)\}""""
"""TargetAccountName ="+({dest_user}[^"]+)""""
"""TargetDomain="+({dest_domain}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```