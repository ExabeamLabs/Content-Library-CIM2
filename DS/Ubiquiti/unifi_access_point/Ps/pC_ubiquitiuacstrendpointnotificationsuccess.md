#### Parser Content
```Java
{
Name = ubiquiti-uac-str-endpoint-notification-success
  Vendor = Ubiquiti
  Product = Unifi Access Point
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """,UAP-AC""", """ntpd: timed out""" ]
  Fields = [
    """:\d\d:\d\d\s+({host}[\w.-]+)""",
    """({event_name}ntpd: timed out)""",
    """({additional_info}ntpd: timed out[^"]+)""",
    """({device_name}UAP-AC)"""
  ]
  DupFields = [ "event_name->operation" ]


}
```