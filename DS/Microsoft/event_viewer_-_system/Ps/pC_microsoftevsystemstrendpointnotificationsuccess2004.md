#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-notification-success-2004
  Vendor = Microsoft
  Product = event viewer - system
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """2004""", """Windows successfully diagnosed a low virtual memory condition""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+EvntSLog""",
    """({event_code}2004)""",
    """({event_name}Windows successfully diagnosed a low virtual memory condition)""",
    """The following programs consumed the most virtual memory:\s*({processes}[^"]*?)\.?"?\s+$""",
  ]


}
```