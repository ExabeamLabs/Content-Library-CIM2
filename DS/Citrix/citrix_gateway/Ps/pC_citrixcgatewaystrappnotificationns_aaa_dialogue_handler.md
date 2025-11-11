#### Parser Content
```Java
{
Name = citrix-cgateway-str-app-notification-ns_aaa_dialogue_handler
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """ns_aaa_dialogue_handler""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^"]+)"*""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){2}\w+)\s+[^:]+:\s*"*({additional_info}[^"]+)"*"""
  ]


}
```