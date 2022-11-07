#### Parser Content
```Java
{
Name = cisco-npe-kv-process-create-success-loggedcommand
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco NPE
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CFGLOG_LOGGEDCMD:""", """logged command:""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """User:\s*({user}[^\s]+)""",
    """logged command:[\s\*]*({process_command_line}({process_name}[^\s]+)?.+?)?[\s\*]*(Source:\s*\/({dest_ip}[A-Fa-f:\d.]+)|$)""",
    """Original Address=({dest_ip}[A-Fa-f:\d.]+)""",
  ]


}
```