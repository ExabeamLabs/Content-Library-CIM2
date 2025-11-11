#### Parser Content
```Java
{
Name = "citrix-cgateway-str-app-notification-diviceup"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """ EVENT DEVICEUP """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}[^"]+)\s+"*"""
  ]


}
```