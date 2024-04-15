#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-success-5140-2-tl"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""eventid":"5140""""
"""<data name='"""
]
Fields = [
"""(?i)({event_code}5140)"""
""""(?i)Computer":"({host}[^"]+)"""
""""(?i)TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""(?i)<Data Name ='SubjectLogonId'>({login_id}.+?)</Data>"""
"""(?i)<Data Name ='SubjectUserName'>({user}.+?)</Data>"""
"""(?i)<Data Name ='SubjectDomainName'>({domain}.+?)</Data>"""
"""(?i)<Data Name ='ObjectType'>({file_type}.+?)</Data>"""
"""(?i)<Data Name ='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\d+))?</Data>"""
"""(?i)<Data Name ='ShareName'>(?:\\\\\*\\)?({share_name}.+?)</Data>"""
"""(?i)<Data Name ='ShareLocalPath'>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+)\\)?({d_name}\s*\S[^\\<]+?))\\?)</Data>"""
"""(?i)({accesses_code}4416)"""
]
DupFields = [
"host->dest_host"
"accesses_code->access"
]
ParserVersion = "v1.0.0"


}
```