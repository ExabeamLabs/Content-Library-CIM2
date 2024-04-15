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
"""Computer="+({dest_host}[^\"]+)""""
"""EventID="+({event_code}[^\"]+)""""
"""EventRecordID="+({event_id}[^\"]+)""""
"""SubjectUserName ="+({user}[^\"]+)""""
"""SubjectDomainName ="+({domain}[^\"]+)""""
"""SubjectLogonId="+({login_id}[^\"]+)""""
"""SubjectUserSid="+({user_sid}[^\"]+)""""
"""TargetDomainName ="+({dest_domain}[^\"]+)""""
"""TargetUserName ="+({dest_user}[^\"]+)""""
"""TargetSid="+({dest_user_sid}[^\"]+)""""
]
DupFields = [
"dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```