#### Parser Content
```Java
{
Name = packetfence-nac-kv-app-notification-role
  Vendor = PacketFence
  Product = PacketFence NAC 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """ role:""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})""",
    """Returning\s+({action}\w+)""",
    """role:\s*({role}\S+)""",
  ]


}
```