#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4724""""
]
Fields = [
"""Computer="+({dest_host}[\w\-.]+)""""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""SubjectDomainName ="+({domain}[^"]+)""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""TargetSid="+({dest_user_sid}[^"]+)""""
"""TargetDomainName ="+({dest_domain}[^"]+)""""
"""TargetUserName ="+({dest_user}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```