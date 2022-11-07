#### Parser Content
```Java
{
Name = cylance-protect-kv-endpoint-activity-device
  ParserVersion = v1.0.0
  Vendor = Cylance
  Product = PROTECT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """ CylancePROTECT """, """Event Type: Device""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z \S+ CylancePROTECT""",
    """Event Type:\s*({event_category}[^,]+)""",
    """Event Name: ({event_name}[^,]+)""",
    """Device Name: ({src_host}[^,]+)""",
    """IP Address: \(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """MAC Address: \(({src_mac}[^\),]+)""",
    """Logged On Users: \((({domain}[^\\\/\)]+)[\\\/]+)?({user}[^\\\/\)\s,]+)""",
    """OS: ({os}[^,]+)""",
    """Zone Names: \(({zone}[^\),]+)""",
  ]


}
```