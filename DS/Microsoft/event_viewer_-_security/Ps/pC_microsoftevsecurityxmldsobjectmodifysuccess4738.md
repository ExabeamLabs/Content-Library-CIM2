#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4738<"""
]
Fields = [
"""<EventID>({event_code}\d+)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Message>({event_name}A user account was changed)"""
"""<Computer>({host}[\w\-\.]+)"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)"""
"""<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)"""
"""<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)"""
"""<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}[^<]+)"""
"""<Data Name\\*=('|")TargetSid('|")>({dest_user_sid}[^<]+)"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)"""
"""<Data Name\\*=('|")OldUacValue('|")>({old_attribute}[^<]+)"""
"""<Data Name\\*=('|")NewUacValue('|")>({new_attribute}[^<]+)"""
"""Changed Attributes:\s*(|({attribute}[^:]+?))\s+SAM Account Name:"""
"""User Account Control:\s*(\\r|\\t|\\n)*(-|({uac_status}[^:]+?))\s*(\\r|\\t|\\n)*User Parameters:"""
"""<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```