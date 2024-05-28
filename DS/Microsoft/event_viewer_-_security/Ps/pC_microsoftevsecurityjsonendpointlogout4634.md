#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-4634
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
 Conditions = [ ""","EventID":""", ""","Account":"""", """An account was logged off""" ]
 Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)"""",
    """({event_code}4634)""",
    """"Activity":"({event_name}[^"]+)""",
    """"Computer":"({src_host}({host}[\w\-.]+))""",
    """"LogonType":"?({login_type}\d+)""",
    """"TargetUserSid":"({user_sid}[^"]+)""",
    """"TargetLogonId":"({login_id}[^"]+)"""
  ]


}
```