#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-permission-modify-4670
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""EventID":4670""", """Permissions on an object were changed"""]
  Fields = [
    """({event_name}Permissions on an object were changed)""",
    """"EventID"*:({event_code}\d+)""",
    """"EventTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"Hostname"*:"*({host}[^"]+)""",
    """"SubjectUserSid"*:"*(SYSTEM|({user_sid}[^"]+))""",
    """"SubjectUserName"*:"*(SYSTEM|({user}[^"]+))""",
    """"SubjectDomainName"*:"*({domain}[^"]+)""",
    """"SubjectLogonId"*:"*({login_id}[^"]+)""",
    """"ProcessID"*:({process_id}[^,"]+)""",
    """"ProcessName"*:"*({process_name}[^"]+)""",
    """"HandleId"*:"*({object_id}[^"]+)""",
    """"ObjectType"*:"*({object_type}[^"]+)""",
    """"ObjectName"*:"*(?:-|({object_name}[^"]+))""",
    """"NewSd"*:"*({attribute}[^"]+)""",
    """"Category"*:"*({category}[^"]+)""",
    """"Opcode"*:"*({severity}[^"]+)""",
]


}
```