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
    """\d\d:\d\d [^\s]+\s({src_mac}[^\s,]+)""",
    """({event_name}ntpd: timed out)""",
    """({additional_info}ntpd: timed out[^"]+)""",
    """({device_name}UAP-AC.+?)\-({firmware_version}\d+\.\d+[^\s:]+)""",
    """waiting for\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
  ]
  DupFields = [ "device_name->product_name", "event_name->operation" ]


}
```