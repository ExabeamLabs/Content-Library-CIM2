#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-4675
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """SIDs were filtered""", """4675""" ]
  Fields = [
    """({event_name}SIDs were filtered)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4675)""",
    """\sTarget Account:\s*(|-|(.+?))\s*Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Trust Information:\s*(|-|(.+?))\s*Trust Direction:\s*(|-|(.+?))\s*Trust Attributes:\s*(|-|(.+?))\s*Trust Type:\s*(|-|({trust_type}.+?))\s*TDO Domain SID:\s*(|-|(.+?))\s*Filtered SIDs:\s*(|-|(.+?))\s*($|<)""",
# DL Fields are removed
  ]
  DupFields = [ "host-> dest_host" ]


}
```