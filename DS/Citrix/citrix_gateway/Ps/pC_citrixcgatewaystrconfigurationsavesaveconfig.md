#### Parser Content
```Java
{
Name = citrix-cgateway-str-configuration-save-saveconfig
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ SAVECONFIG """ ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*""",
    """GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")"""

  ]


}
```