#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4740</EventID>"""
"""<Data Name ='TargetSid'>"""
]
Fields = [
"""SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name ='SubjectUserName'>({src_user}[^<]+)</Data>"""
"""<Data Name ='SubjectDomainName'>({src_domain}[^<]+)</Data>"""
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"""
"""<Data Name ='TargetSid'>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name ='TargetUserName'>(?=\w)({user}[^<]+)</Data>"""
"""<Data Name ='SubjectDomainName'>(?=\w)({domain}[^<]+)</Data>"""
  ]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```