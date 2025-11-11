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
    """"(Hostname|Computer)":"({dest_host}({host}[\w.-]+?))"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}User initiated logoff)""",
    """"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"TargetDomainName":"({dest_domain}({domain}[^"]+))"""",
    """"TargetLogonId":"({dest_login_id}({login_id}[^"]+))"""",
    """"Keywords":({result}[^,]+)"""
    """"TargetUserSid":"({dest_user_sid}({user_sid}[^"]+))""",
    """"ProcessID":({process_id}\d+)""",
    """"ThreadID":({thread_id}\d+)"""
  ]


}
```