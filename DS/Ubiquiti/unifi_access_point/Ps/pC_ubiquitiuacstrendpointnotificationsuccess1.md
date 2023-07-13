#### Parser Content
```Java
{
Name = ubiquiti-uac-str-endpoint-notification-success-1
  Vendor = Ubiquiti
  Product = Unifi Access Point
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """,US-48""", """switch:""" ]
  Fields = [
    """:\d\d:\d\d\s+({host}[\w.-]+)""",
    """\d\d:\d\d [^\s]+\s({src_mac}[^\s,]+)""",
    """({additional_info}switch:[^"]+)""",
    """({device_name}US-48.+?)\-({firmware_version}\d+\.\d+[^\s:]+)""",
    """({device_type}switch)"""
  ]
  DupFields = [ "device_name->product_name" ]


}
```