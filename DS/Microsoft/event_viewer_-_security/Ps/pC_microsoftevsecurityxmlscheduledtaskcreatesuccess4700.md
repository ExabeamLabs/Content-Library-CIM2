#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4700"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4700</EventID>"""
"""<Data Name"""
"""SubjectUserName"""
"""<Message>A scheduled task was enabled"""
]
Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)</Computer>"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""({event_code}4700)"""
"""({event_name}A scheduled task was enabled)"""
"""<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
"""<Data Name\\*=('|")TaskName('|")>({task_name}[^<]+)<"""
"""<Data Name\\*=('|")TaskContent('|")>({additional_info}[^<]+)<"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"
DupFields = [ "host-> dest_host", "user->src_user", "domain->src_domain"]


}
```