#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-create-success-5137"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>5137</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_code}5137)"""
"""<Computer>({host}[\w\-\.]+)</Computer>"""
"""<Keywords>({result}[^<]+)</Keywords>"""
"""<Data Name ='SubjectUserSid'>(|({user_sid}[^<]+?))</Data>"""
"""<Data Name ='SubjectUserName'>(|({user}[^<]+?))</Data>"""
"""<Data Name ='SubjectDomainName'>(|({domain}[^<]+?))</Data>"""
"""<Data Name ='SubjectLogonId'>(|({login_id}[^<]+?))</Data>"""
"""<Data Name ='ObjectDN'>(|({object_dn}[^<]+?))</Data>"""
"""<Data Name ='ObjectClass'>(|({ds_object_class}[^<]+?))</Data>"""
"""({event_name}A directory service object was created)"""
]
DupFields = [ 
   "host->dest_host" 
]
ParserVersion = "v1.0.0"


}
```