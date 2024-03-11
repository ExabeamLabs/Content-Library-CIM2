#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-group-modify-success-4755
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"EventID":4755""", """A security-enabled universal group was changed""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}A security-enabled universal group was changed)""",
    """"SubjectUserName":"({user}[^"]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"Keywords":({result}[^,]+)"""
    """"TargetUserName":"({group_name}[^"]+)"""
    """"TargetDomainName":"({group_domain}[^"]+)""",
    """"TargetSid":"({group_id}[^"]+)""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)"""
  ]


}
```