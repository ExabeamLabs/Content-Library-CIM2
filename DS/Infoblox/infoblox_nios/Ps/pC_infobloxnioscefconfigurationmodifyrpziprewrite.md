#### Parser Content
```Java
{
Name = infoblox-nios-cef-configuration-modify-rpziprewrite
  Vendor = Infoblox
  Product = Infoblox NIOS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """|Infoblox|NIOS|""", """ named[""", """ qtype=""", """ msg="""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({event_code}[^\|]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d ({host}\S+) named""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """qtype=({dns_query_type}.+?)\s+(\w+=|$)""",
    """msg="rpz ({request_type}\S+) ({dns_response_code}\S+) ({operation}\S+) ({query}.+?)\s*\[[^\]]+\] via ([^"]+)""", #dl field removed
    """app=({app}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "query->domain" ]
  ParserVersion = "v1.0.0"


}
```