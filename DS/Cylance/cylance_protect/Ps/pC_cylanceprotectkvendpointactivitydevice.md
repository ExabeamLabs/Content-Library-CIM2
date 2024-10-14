#### Parser Content
```Java
{
Name = cylance-protect-kv-endpoint-activity-device
  ParserVersion = v1.0.0
  Vendor = Cylance
  Product = Cylance PROTECT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """ CylancePROTECT """, """Event Type: Device""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z \S+ CylancePROTECT""",
    """Event Type:\s*({event_category}[^,]+)""",
    """Event Name: ({event_name}[^,]+)""",
    """Device Name: ({src_host}[^,]+)""",
    """IP Address: \(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """MAC Address: \(({src_mac}[^\),]+)""",
    """Logged On Users: \((({domain}[^\\\/\)]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """OS: ({os}[^,]+)""",
    """Zone Names: \(({zone}[^\),]+)""",
  ]


}
```