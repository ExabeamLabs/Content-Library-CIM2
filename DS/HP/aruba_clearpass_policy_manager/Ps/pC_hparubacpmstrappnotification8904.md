#### Parser Content
```Java
{
Name = hp-arubacpm-str-app-notification-8904
  ParserVersion = v1.0.0
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""Event|8904|""", """LOG_INFO|MSTR""", """|CDP neighbor""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """({host}[\w\-\.]+)\s*cdpd""",
    """({event_code}8904)""",
    """({event_name}MSTR)""",
    """({additional_info}CDP neighbor[^"$]+)("|$)"""
  ]


}
```