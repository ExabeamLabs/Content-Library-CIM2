#### Parser Content
```Java
{
Name = packetfence-p-kv-app-notification-status
  Vendor = PacketFence
  Product = PacketFence 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """, Status:""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})""",
    """PID:\s*"({email_address}[^\s@"]+@[^\s@"]+)""",
    """Status:\s*({action}\w+)""",
# vlan is removed
  ]


}
```