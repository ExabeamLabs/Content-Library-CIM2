#### Parser Content
```Java
{
Name = citrix-cgateway-kv-app-notification-monitorup
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ EVENT MONITORUP """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")"""
    """({event_name}EVENT MONITORUP)"""
  ]
  DupFields = ["host->src_host"]


}
```