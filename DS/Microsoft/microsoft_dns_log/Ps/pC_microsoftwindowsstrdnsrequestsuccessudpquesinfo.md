#### Parser Content
```Java
{
Name = "microsoft-windows-str-dns-request-success-udpquesinfo"
  Vendor = Microsoft
  Product = Microsoft DNS Log
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """UDP question info at """, """Buf length =""" ]
  Fields = [
    """({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (AM|am|PM|pm))""",
    """({protocol}UDP)\s+({operation}Rcv)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Remote addr\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),\s*port\s*({src_port}\d+)""",
    """XID\s+0x({query_id}[\da-fA-F]+)""",
    """QTYPE\s+({dns_query_type}\w+)""",
    """RCODE\s+[^(]*?\(({result}[^(]+)\)""",
    """QUESTION SECTION:.*?Name\s+"({dns_query}[^"]+)"""",
    """Buf length\s*=\s*\S+\s*\(({bytes}\d+)""",
    """ANSWER SECTION:(\s*empty|.+?DATA\s+({response}\S+))"""
  ]
  ParserVersion = "v1.0.0"


}
```