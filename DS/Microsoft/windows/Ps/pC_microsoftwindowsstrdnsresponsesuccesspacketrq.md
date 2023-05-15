#### Parser Content
```Java
{
Name = microsoft-windows-str-dns-response-success-packetrq
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "dd/MM/yyyy HH:mm:ss"
  Conditions = [
""" PACKET """,
""" R Q ["""
  ]
  Fields = [
    """({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2}(\S+)?\s+(am|AM|pm|PM))\s+\S+\s+PACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\S+\s+(R)? (Q|U)\s+\[\S+\s+({dns_response_flags}.+?)\s+({dns_response_code}\S+)\]\s+({dns_query_type}\S+)\s+({dns_query}[^\s]+)""",
    """<Identifier>\S+\s+({host}\S+?)<\/Identifier>""",
    """(({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2})|({=time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d[+-]\d\d:\d\d))\s+\S+\s+PACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\S+\s+R\s+Q\s+\[\S+\s+(\s|({dns_response_flags}.+?))\s+({dns_response_code}\S+)\]\s+({dns_query_type}\S+)\s+({dns_query}.+?)\s"""
  ]


}
```