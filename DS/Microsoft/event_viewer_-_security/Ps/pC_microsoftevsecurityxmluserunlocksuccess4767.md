#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-unlock-success-4767
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<EventID>4767</EventID>"""
"""<Event xmlns='"""
]
Fields = [
"""<Computer>({host}.+?)</Computer>"""
"""<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'/>"""
"""<Data Name ='SubjectLogonId'>\s*({login_id}.+?)\s*</Data>"""
"""<Data Name ='SubjectUserName'>\s*(SYSTEM|({user}[^\s]+?))\s*</Data>"""
"""<Data Name ='SubjectDomainName'>\s*({domain}[^\s]+?)\s*</Data>"""
"""<Data Name ='SubjectUserSid'>\s*({user_sid}[^\s]+?)\s*</Data>"""
"""<Data Name ='TargetDomainName'>\s*({dest_domain}[^\s]+?)\s*</Data>"""
"""<Data Name ='TargetUserName'>\s*({dest_user}[^\s]+?)\s*</Data>"""
"""<Data Name ='TargetSid'>\s*({dest_user_sid}.+?)</Data>\s*"""
"""({event_code}4767)"""
  ]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```