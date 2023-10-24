#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-success-5140-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""EventID":"5140""""
"""<Data Name"""
]
Fields = [
"""({event_code}5140)"""
""""Computer":"({host}[^"]+)"""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Data Name\\*='SubjectLogonId'>({login_id}.+?)</Data>"""
"""<Data Name\\*='SubjectUserName'>({user}[\w\.\-]{1,40}\$?)</Data>"""
"""<Data Name\\*='SubjectDomainName'>({domain}.+?)</Data>"""
"""<Data Name\\*='ObjectType'>({file_type}.+?)</Data>"""
"""<Data Name\\*='IpAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
"""<Data Name\\*='ShareName'>(?:\\\\\*\\)?({share_name}.+?)</Data>"""
"""<Data Name\\*='ShareLocalPath'>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+)\\)?({d_name}\s*\S[^\\<]+?))\\?)</Data>"""
"""({accesses_code}4416)"""
"""'IpPort'>({src_port}\d+)"""
"""Source Port(=|:)\s*(\\t)*({src_port}\d+)"""
]
DupFields = [
"host->dest_host"
"accesses_code->access"
]
ParserVersion = "v1.0.0"


}
```