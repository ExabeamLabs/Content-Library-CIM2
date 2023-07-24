#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-audit-policy-modify-4904
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""EventID":4904""", """An attempt was made to register a security event source"""]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_name}An attempt was made to register a security event source)""",
    """"HostName":"({host}[^"]+)"""",
    """({event_code}4904)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SeverityValue":({severity}[^,]+)""",
    """"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"ProcessID":({process_id}[^"]+)"""",
# audit_name is removed
  ]


}
```