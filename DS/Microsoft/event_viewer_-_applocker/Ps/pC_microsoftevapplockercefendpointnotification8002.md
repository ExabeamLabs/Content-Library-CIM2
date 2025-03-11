#### Parser Content
```Java
{
Name = microsoft-evapplocker-cef-endpoint-notification-8002
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Applocker
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":""", """8002""", """A process was allowed to run""" ]
  Fields = [
    """"Activity":"(\d+\s+-\s+)?({event_name}[^"]+?)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)""",
    """"EventID":"?({event_code}\d+)""",
    """"Account":"(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """<TargetLogonId>({login_id}.+?)</TargetLogonId>""",
    """"TargetLogonId":"({login_id}[^"]+)""",
    """"TargetUserSid":"({user_sid}[^"]+)""",
    """"TargetUser":"(({user_sid}S-[^\"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"FileHash":"({hash_md5}[^"]+)""",
    """"FilePath":"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\\\/]+))?))"""",
# fqbn is removed
    """"Process":"({process_name}[^"]+)"""
  ]


}
```