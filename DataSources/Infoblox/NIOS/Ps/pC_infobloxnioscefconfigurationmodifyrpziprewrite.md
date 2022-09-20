#### Parser Content
```Java
{
Name = infoblox-nios-cef-configuration-modify-rpziprewrite
  Vendor = Infoblox
  Product = NIOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Infoblox|NIOS|""", """ named[""", """ qtype=""", """ msg="""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({event_code}[^\|]+)""",
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """spt=({src_port}\d+)""",
    """qtype=({query_type}.+?)\s+(\w+=|$)""",
    """msg="rpz ({request_type}\S+) ({dns_response_code}\S+) ({operation}\S+) ({query}.+?)\s*\[[^\]]+\] via ([^"]+)""", #dl field removed
    """app=({app}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "query->domain" ]
  ParserVersion = "v1.0.0"


}
```