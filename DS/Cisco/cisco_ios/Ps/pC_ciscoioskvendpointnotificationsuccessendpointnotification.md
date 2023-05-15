#### Parser Content
```Java
{
Name = cisco-ios-kv-endpoint-notification-success-endpointnotification
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ %IOSXE-3-PLATFORM: """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """src_addr:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),\s*src_port:\s*({src_port}\d{1,5}),""",
    """dest_addr:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),\s*dst_port:\s*({dest_port}\d{1,5})""",
    """%IOSXE-3-PLATFORM:\s*({additional_info}[^"]+)\s""" 
  ]


}
```