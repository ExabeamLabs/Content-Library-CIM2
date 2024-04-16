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
    """\d\d:\d\d [^\s]+\s({src_mac}[^\s,]+)""",
    """wevent\[\d+\]:\s*({additional_info}[^"]+)""",
    """({device_name}UAP-AC.+?)\-({firmware_version}\d+\.\d+[^\s:]+)""",
  ]
  DupFields = [ "device_name->product_name" ]


}
```