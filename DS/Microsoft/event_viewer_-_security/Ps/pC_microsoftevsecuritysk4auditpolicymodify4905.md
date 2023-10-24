#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-audit-policy-modify-4905
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""EventID":4905""", """An attempt was made to unregister a security event source"""]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_name}An attempt was made to unregister a security event source)""",
    """"HostName":"({host}[^"]+)"""",
    """({event_code}4905)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SeverityValue":({severity}[^,]+)""",
    """"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"ProcessID":({process_id}[^"]+)"""",
# src_name is removed
# src_id is removed
  ]


}
```