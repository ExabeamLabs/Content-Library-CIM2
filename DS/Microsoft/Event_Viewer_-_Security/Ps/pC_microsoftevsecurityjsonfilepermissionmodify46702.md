#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-permission-modify-4670-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""event_id":4670""", """Permissions on an object were changed"""]
  Fields = [
    """({event_name}Permissions on an object were changed)""",
    """"event_id"*:({event_code}\d+)""",
    """"@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"hostname"*:"*({host}[^"]+)""",
    """"(?:winlog\.)?computer_name"*:"*({src_host}[^"]+)""",
    """"SubjectUserSid"*:"*(SYSTEM|({user_sid}[^"]+))""",
    """"SubjectUserName"*:"*(SYSTEM|({user}[^"]+))""",
    """"SubjectDomainName"*:"*({domain}[^"]+)""",
    """"SubjectLogonId"*:"*({login_id}[^"]+)""",
    """"ProcessId"*:({process_id}\d+)""",
    """"ProcessName"*:"*({process_name}[^"]+)""",
    """"HandleId"*:"*({object_id}[^"]+)""",
    """"ObjectType"*:"*({object_type}[^"]+)""",
    """"ObjectName"*:"*(?:-|({object_name}[^"]+))""",
    """"NewSd"*:"*({attribute}[^"]+)""",
    """"opcode"*:"*({severity}[^"]+)"""
]


}
```