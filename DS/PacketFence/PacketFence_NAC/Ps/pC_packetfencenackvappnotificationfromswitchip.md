#### Parser Content
```Java
{
Name = packetfence-nac-kv-app-notification-fromswitchip
  Vendor = PacketFence
  Product = PacketFence NAC 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """from switch_ip""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})""",
    """from switch_ip\s*=>\s*\(({dest_ip}[A-Fa-f:\d.]+)""",
    """port\s*=>\s*(0|({dest_port}\d+))""",
    """packetfence:\s*\w+\s+\S+\s+\S+\s+({event_name}[^\[\]:"\-]+)""",
  ]


}
```