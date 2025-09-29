#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-outofsync
	ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """monitor[""", """Type: NTP Synchronization,""", """The NTP service is out of synchronization""" ]
  Fields = [      
	  """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}[a-fA-F\d.:]+?)\s+({additional_info}[^~]+?)\s*$""",
    """({event_name}The NTP service is out of synchronization)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```