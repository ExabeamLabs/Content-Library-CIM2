#### Parser Content
```Java
{
Name = ubiquiti-uac-str-endpoint-notification-success-2
  Vendor = Ubiquiti
  Product = Unifi Access Point
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """,UAP-AC""", """stahtd:""", """"message_type":"STA_ASSOC_TRACKER"""" ]
  Fields = [
    """:\d\d:\d\d\s+({host}[\w.-]+)""",
    """"mac":"({src_mac}[^"]+)""",
    """({device_name}UAP-AC.+?)\-({firmware_version}\d+\.\d+[^\s:]+)""",
    """"message_type":"({event_category}[^"]+)""",
    """"event_type":"({sub_category}[^"]+)""",
    """"event_id":"({event_id}[^"]+)""",
    """"avg_rssi":"({additional_info}[^"]+)"""
  ]
  DupFields = [ "device_name->product_name" ]


}
```