#### Parser Content
```Java
{
Name = pan-gp-leef-app-activity-system
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """LEEF:""", """|Palo Alto Networks|PAN-OS Syslog Integration|""" ,"""|cat=SYSTEM|""", """|Subtype="""]
  Fields = [
    """\|ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """User name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """IP\s*({src_ip}[A-Fa-f:.\d]+),\s*port\s*({src_port}\d+)""",
    """DeviceName =({host}[\w\-.]+)""",
    """Severity=({severity}[^\s|]+)""",
    """connected to server\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
    """initiated by:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Client OS ( version)?.+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```