#### Parser Content
```Java
{
Name = ubiquiti-uac-str-endpoint-notification-success-3
  Vendor = Ubiquiti
  Product = Unifi Access Point
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """,UAP-AC""", """wevent""" ]
  Fields = [
    """:\d\d:\d\d\s+({host}[\w.-]+)""",
    """wevent\[\d+\]:({additional_info}[^"]+)""",
    """({device_name}UAP-AC)"""
  ]


}
```