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
    """({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2}(\S+)?\s+(am|AM|pm|PM))\s+\S+\s+PACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}[a-fA-F\d.:]+)\s+\S+\s+(R)? (Q|U)\s+\[\S+\s+({dns_response_flags}.+?)\s+({dns_response_code}\S+)\]\s+({dns_query_type}\S+)\s+({dns_query}[^\s]+)""",
    """<Identifier>\S+\s+({host}\S+?)<\/Identifier>""",
    """({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2})\s+\S+\s+PACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}[a-fA-F\d.:]+)\s+\S+\s+R\s+Q\s+\[\S+\s+(\s|({dns_response_flags}.+?))\s+({dns_response_code}\S+)\]\s+({dns_query_type}\S+)\s+({dns_query}.+?)\s"""
  ]


}
```