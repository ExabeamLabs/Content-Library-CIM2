#### Parser Content
```Java
{
Name = cisco-ios-kv-endpoint-notification-success-endpointnotification
  Vendor = Cisco
  Product = cisco ios
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ %IOSXE-3-PLATFORM: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """src_addr:\s*({src_ip}[A-Fa-f\d:.]+?),\s*src_port:\s*({src_port}\d{1,5}),""",
    """dest_addr:\s*({dest_ip}[A-Fa-f\d:.]+?),\s*dst_port:\s*({dest_port}\d{1,5})""",
    """%IOSXE-3-PLATFORM:\s*({additional_info}[^"]+)\s""" 
  ]


}
```