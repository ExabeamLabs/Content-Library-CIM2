#### Parser Content
```Java
{
Name = cyberark-epm-json-user-privilege-use-success-setname
Vendor = CyberArk
Product = CyberArk Endpoint Privilege Manager
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""RestrAccessEvent":"""
""""setName":""""
""""RestrictedObjectId":""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d\d:\d\d)""",
"""\d\d:\d\d\s({host}[^\s]+)\sLOGSTASH""",
"""({event_name}RestrAccessEvent)""",
""""Size"+:"+({bytes}\d+)""",
""""computerName"+:"+({src_host}[^"]+)""",
""""Description"+:"+({additional_info}[^"]+)""",
""""PolicyName"+:"+({policy_name}[^"]+)""",
""""@user"+:"+(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
""""@OsProcessId"+:"+({process_id}\d+)""",
""""Path"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
""""@allowed"+:"+({result}[^"]+)""",
""""eventId"+:"+({event_code}[^"]+)""",
""""RestrictedObjectId"+:"+\{({object_id}[^"}]+)""",
  ]


}
```