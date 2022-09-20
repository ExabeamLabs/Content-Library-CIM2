#### Parser Content
```Java
{
Name = pan-gp-leef-app-activity-system
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  ParserVersion = v1.0.0
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """LEEF:""", """|Palo Alto Networks|PAN-OS Syslog Integration|""" ,"""|cat=SYSTEM|""", """|Subtype="""]
  Fields = [
    """\|ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """User name:\s*({user}[\w.'\-\\$]+)""",
    """IP\s*({src_ip}[A-Fa-f:.\d]+),\s*port\s*({src_port}\d+)""",
    """DeviceName =({host}[\w\-.]+)""",
    """Severity=({severity}[^\s|]+)""",
    """connected to server\s({dest_ip}[A-Fa-f:\d.]+):({dest_port}\d+)""",
    """initiated by:\s*({src_ip}[A-Fa-f.:\d]+)""",
    """Client OS ( version)?.+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]


}
```