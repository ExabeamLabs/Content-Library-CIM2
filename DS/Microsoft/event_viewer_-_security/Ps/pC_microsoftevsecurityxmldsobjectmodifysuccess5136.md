#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
"""<EventID>5136</EventID>"""
"""<Event xmlns="""
]
Fields = [
"""<Computer>({host}({dest_host}[\w\-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d*Z('|")/>"""
"""<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
"""<Data Name\\*=('|")SubjectLogonId('|")>\s*({login_id}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")SubjectUserName('|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>\s*({domain}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")AttributeLDAPDisplayName('|")>\s*({attribute}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ObjectClass('|")>\s*({object_type}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ObjectDN('|")>\s*({ds_object_dn}[^<]+?)\s*</Data>"""
"""({event_code}5136)"""
"""<Message>({event_name}A directory service object was modified)"""
"""<Data Name\\*=('|")DSName('|")>(|({ds_name}[^<]+?))</Data>"""
"""<Data Name\\*=('|")DSType('|")>(|({ds_type}[^<]+?))</Data>"""
"""<Level>({run_level}[^<]+)<"""
"""AttributeValue("|')>({attribute_value}[^"'<]+)</Data>"""
"""<Data Name(\\)?=('|")OperationType('|")>({operation_type}[^<]+)"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```