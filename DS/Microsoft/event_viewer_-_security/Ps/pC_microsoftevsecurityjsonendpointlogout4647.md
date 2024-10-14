#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-4647
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"EventID":4647""", """User initiated logoff""" ]
  Fields = [
    """"EventTime":({time}\d{10})""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}User initiated logoff)""",
    """"TargetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"TargetDomainName":"({domain}[^"]+)"""",
    """"TargetLogonId":"({login_id}[^"]+)"""",
    """"Keywords":({result}[^,]+)"""
    """"TargetUserSid":"({user_sid}[^"]+)""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```