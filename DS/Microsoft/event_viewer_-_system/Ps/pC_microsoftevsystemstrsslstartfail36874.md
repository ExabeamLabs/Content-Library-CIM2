#### Parser Content
```Java
{
Name = microsoft-evsystem-str-ssl-start-fail-36874
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """(36874)""", """connection request was received from a remote client application""" ]
  Fields = [
    """({event_code}36874)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\s+({dest_host}({host}[\w.\-]+))\s+EvntSLog""",
    """({event_name}The \w+ connection request has failed)""",
  ]


}
```