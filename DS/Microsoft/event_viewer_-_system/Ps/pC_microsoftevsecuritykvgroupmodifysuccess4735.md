#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-modify-success-4735
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """4735""", """A security-enabled local group was changed""" ]
  Fields = [
    """({event_name}A security-enabled local group was changed)""",
    """({event_code}4735)""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)"""
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """\srt=({time}\d{13})""",
    """"(?i)Computer(Name)?":\s*"({host}[^"]+)"""",
    """"(?i)HostName":\s*"({host}[^"]+)"""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)\s+Account Name:""",
    """Subject:.+?Account Name:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Subject:.+?Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:.+?Logon ID:\s*({login_id}[^\s]+)""",
    """Group:\s+Security ID:\s+({group_id}[^\s]+)""",
    """Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)""",
  ]


}
```