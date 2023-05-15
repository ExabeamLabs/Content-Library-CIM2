#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-privilege-modify-success-4705
ParserVersion = v1.0.0
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>4705</EventID>""",
"""A user right was removed"""
]
Fields = [
"""<EventID>({event_code}[^<]+)<\/EventID>"""
"""<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Provider Name\\*='({provider_name}[^']+)'"""
"""<Keywords>({result}[^<]+)<\/Keywords>"""
"""<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
"""<Execution ProcessID\\*='({process_id}[^']+)"""
"""ThreadID\\*='({thread_id}[^']+)"""
"""<Computer>({host}[^<]+?)<"""
"""<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)<"""
"""<Data Name\\*='SubjectUserName'>({user}[^<]+)<"""
"""<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<"""
"""<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<"""
"""<Data Name\\*='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
"""<Data Name\\*='PrivilegeList'>({privileges}[^<]+?)<"""
"""<Message>({event_name}[^.<]+)\s*""",
]


}
```