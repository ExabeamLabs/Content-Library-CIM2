#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-create-success-5137"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
"""<EventID>5137</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
"""({event_code}5137)"""
"""<Computer>({dest_host}({host}[\w\-\.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Keywords>({result}[^<]+)</Keywords>"""
"""<Data Name\\*='SubjectUserSid'>(|({user_sid}[^<]+?))</Data>"""
"""<Data Name\\*='SubjectUserName'>(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>"""
"""<Data Name\\*='SubjectDomainName'>(|({domain}[^<]+?))</Data>"""
"""<Data Name\\*='SubjectLogonId'>(|({login_id}[^<]+?))</Data>"""
"""<Data Name\\*=("|')ObjectDN("|')>(|({ds_object_dn}[^<]+?))</Data>"""
"""<Data Name\\*='ObjectClass'>(|({object_type}[^<]+?))</Data>"""
"""({event_name}A directory service object was created)"""
"""<Data Name\\*=("|')DSName("|')>(|({ds_name}[^<]+?))</Data>"""
"""<Data Name\\*=("|')DSType("|')>(|({ds_type}[^<]+?))</Data>"""
"""<Level>({run_level}[^<]+)"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```