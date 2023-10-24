#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-delete-success-4726-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4726"""
"""SubjectUserSid":"""
"""A user account was deleted"""
]
Fields = [
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
""""Hostname":"({host}[\w\-.]+)""""
"""({event_name}A user account was deleted)"""
""""TargetUserName":"({dest_user}[^"]+)""""
""""TargetDomainName":"({dest_domain}[^"]+)""""
""""TargetSid":"({dest_user_sid}[^"]+)""""
""""EventID":({event_code}4726)"""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({user}[\w\.\-]{1,40}\$?)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""SubjectLogonId":"({login_id}[^"]+)""""
]
DupFields = [
"host->dest_host"
"dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```