#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-handle-close-4658-tl"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""4658"""
"""<data name='"""
"""the handle to an object was closed"""
]
Fields = [
"""(?i)<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""(?i)"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""(?i)({event_code}4658)"""
"""(?i)({event_name}The handle to an object was closed)"""
"""(?i)"Activity":"({event_name}[^"]+)"""
"""(?i)(<|")Computer(>|"):?"?({host}[^"<]+)"""
"""(?i)<Data Name ='SubjectUserSid'>({user_sid}[^<>]+)</Data>"""
"""(?i)<Data Name ='SubjectUserName'>(SYSTEM|({user}[^<>]+))</Data>"""
"""(?i)<Data Name ='SubjectDomainName'>(NT AUTHORITY|({domain}[^<>]+))</Data>"""
"""(?i)<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"""
"""(?i)<Data Name ='ObjectServer'>({object_server}[^<>]+)</Data>"""
"""(?i)<Data Name ='ProcessId'>({process_id}[^<>]+)</Data>"""
"""(?i)<Data Name ='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>"""
"""(?i)({operation_type}closed)"""
"""(?i)<Data Name ='HandleId'>({object_id}[^<>]+)</Data>"""
]


}
```