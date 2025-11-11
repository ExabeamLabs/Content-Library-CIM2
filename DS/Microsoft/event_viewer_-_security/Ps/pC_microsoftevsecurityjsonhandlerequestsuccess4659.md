#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-request-success-4659
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A handle to an object was requested with intent to delete""", """"EventID":4659"""]
  Fields = [
    """({event_name}A handle to an object was requested with intent to delete)""",
    """({event_code}4659)""",
    """"Hostname":"({dest_host}({host}[^"]+))"""",
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"SubjectUserSid":"({user_sid}[^"]+)""""
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"ObjectServer":"({object_server}[^"]+)"""",
    """"ObjectType":"({object_type}[^"]+)"""",
    """"ObjectName":"({object}[^"]+)"""",
    """"HandleId":"({object_id}[^"]+)"""",
    """"ProcessID":({process_id}[^,]+),""",
  ]


}
```