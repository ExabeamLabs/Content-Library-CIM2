#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-delete-success-4743"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""A computer account was deleted"""
"""<EventID>4743</EventID>"""
]
Fields = [
"""({event_name}A computer account was deleted)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
"""({event_code}4743)"""
"""Subject:[^=]+?\sAccount Name:\s*(|-|({user}[^=]+?))\s*Account Domain:\s*(|-|({domain}[^=]+?))\s*Logon ID:\s*(|-|({login_id}[^=]+?))\s*Target Computer:[^=]+?\sAccount Name:\s*(|-|({dest_user}[^=]+?))\s*Account Domain:\s*(|-|({object_dn}[^\"]+?))\s*Additional Information:"""
"""\sTarget Computer:[^=]+?Account Name:\s*({src_host}[^$:]+?)\$"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```