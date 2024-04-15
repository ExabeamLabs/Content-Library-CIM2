#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4738"""
"""A user account was changed"""
]
Fields = [
"""({event_name}A user account was changed)"""
"""({event_code}4738)"""
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
""""Host(N|n)ame":"({host}[^"]+)""""
""""+EventTime"+:"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"+"""
""""SeverityValue":({severity}[^,]+)""""
""""TargetUserName":"({dest_user}[^"]+)""""
""""TargetDomainName":"({dest_domain}[^"]+)""""
""""TargetSid":"({target_sid}[^"]+)""""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({user}[^"]+)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""SubjectLogonId":"({login_id}[^"]+)""""
""""+Category"+:"+({category}[^"]+)"+"""
""""+Message"+:"+({additional_info}[^"]+)"+"""
""""+EventType"+:"+({result}[^"]+)"+"""
]
ParserVersion = "v1.0.0"


}
```