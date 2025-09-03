#### Parser Content
```Java
{
Name = citrix-cgateway-str-app-notification-ppe
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ ROUTING """, """-PPE-""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*"*(Command?\s*"*([^"]+))?"*\s*({additional_info}[^"]+)"*""",# cmd is removed
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*"*(Command?\s*"*([^"]+))?"*\s*({additional_info}.+?)"*\s+($|")"""# cmd is removed
]


}
```