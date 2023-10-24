#### Parser Content
```Java
{
Name = citrix-cgateway-str-app-notification-monitordown
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ EVENT MONITORDOWN """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")"""
  ]
  DupFields = ["host->src_host"]


}
```