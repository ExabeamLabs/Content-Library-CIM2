#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-wls"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4726""""
]
Fields = [
"""Computer="+({dest_host}[\w\-.]+)""""
"""EventID="+({event_code}[^\"]+)""""
"""EventRecordID="+({event_id}[^\"]+)""""
"""SubjectUserName ="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""SubjectDomainName ="+({src_domain}({domain}[^\"]+))""""
"""SubjectLogonId="+({login_id}[^\"]+)""""
"""SubjectUserSid="+({user_sid}[^\"]+)""""
"""TargetDomainName ="+({dest_domain}[^\"]+)""""
"""TargetUserName ="+({account_name}({dest_user}[^\"]+))""""
"""TargetSid="+({dest_user_sid}[^\"]+)""""
]
ParserVersion = "v1.0.0"


}
```