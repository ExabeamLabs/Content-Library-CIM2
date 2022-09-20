#### Parser Content
```Java
{
Name = packetfence-nac-str-app-notification-cantfindprovisionerfor
  Vendor = PacketFence
  Product = PacketFence NAC 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """Can't find provisioner for""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """({event_name}Can't find provisioner for ({src_mac}(\w{2}:){5}\w{2}))""",
  ]


}
```