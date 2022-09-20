#### Parser Content
```Java
{
Name = packetfence-nac-str-app-notification-line
  Vendor = PacketFence
  Product = PacketFence NAC 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """packetfence:""", """ line """ ]
  Fields = [
    """\s({host}[\w\-.]+)\s+packetfence:""",
    """\s({app}packetfence)""",
    """packetfence:\s*({event_category}\w+)""",
    """packetfence:\s*\w+\s+\S+\s+({event_name}[^\[\]:"\-]+)""",
    """packetfence:\s*.*?\s+(|({file_path}({file_dir}\/[^"]*?)[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?)))\s+line""",
# line_num is removed
  ]


}
```