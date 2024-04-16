#### Parser Content
```Java
{
Name = packetfence-p-kv-app-notification-fromswitchip
  Vendor = PacketFence
  Product = PacketFence 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """from switch_ip""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})""",
    """from switch_ip\s*=>\s*\(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """port\s*=>\s*(0|({dest_port}\d+))""",
    """packetfence:\s*\w+\s+\S+\s+\S+\s+({event_name}[^\[\]:"\-]+)""",
  ]


}
```