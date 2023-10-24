#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<EventID>5136</EventID>"""
"""<Event xmlns="""
]
Fields = [
"""<Computer>({host}({dest_host}[\w-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d*Z('|")/>"""
"""<Data Name\\*=('|")SubjectLogonId('|")>\s*({login_id}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")SubjectUserName('|")>\s*(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s*</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>\s*({domain}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")AttributeLDAPDisplayName('|")>\s*({attribute}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ObjectClass('|")>\s*({ds_object_class}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ObjectDN('|")>\s*({ds_object_dn}[^<]+?)\s*</Data>"""
"""({event_code}5136)"""
"""<Message>({event_name}A directory service object was modified)"""
"""<Data Name\\*=('|")DSName('|")>(|({ds_name}[^<]+?))</Data>"""
"""<Data Name\\*=('|")DSType('|")>(|({ds_type}[^<]+?))</Data>"""
]
ParserVersion = "v1.0.0"


}
```