#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-privilege-assign-success-4704
ParserVersion = v1.0.0
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>4704</EventID>""",
"""Microsoft-Windows-Security-Auditing"""
]
Fields = [
"""<EventID>({event_code}[^<]+)<\/EventID>"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
"""<Provider Name\\*=('|")({provider_name}[^'"]+)('|")"""
"""<Keywords>({result}[^<]+)<\/Keywords>"""
"""<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
"""<Execution ProcessID\\*=('|")({process_id}[^"']+)"""
"""ThreadID\\*=('|")({thread_id}[^'"]+)"""
"""<Computer>({host}[^<]+?)<"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<"""
"""<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
"""<Data Name\\*=('|")PrivilegeList('|")>({privileges}[^<]+?)<"""
"""<Message>({event_name}[^.<]+)\s*""",
"""<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]


}
```