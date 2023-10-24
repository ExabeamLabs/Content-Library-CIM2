#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-modify-4755"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4755""", """A security-enabled universal group was changed""" ]
  Fields = [
    """({event_name}A security-enabled universal group was changed)""",
    """({event_code}4755)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s""",
    """\srt=({time}\d{13})""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)\s+Account Name:""",
    """Subject:.+?Account Name:\s*(-|({user}[\w\.\-]{1,40}\$?))""",
    """Subject:.+?Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:.+?Logon ID:\s*({login_id}[^\s]+)""",
    """Group:\s+Security ID:\s+({group_id}[^\s]+)""",
    """Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)""",
  ]


}
```