#### Parser Content
```Java
{
Name = "microsoft-windows-str-dns-request-success-packetqm"
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft DNS Log
  TimeFormat = "M/d/yyyy H:mm:ss a"
  Conditions = [
""" PACKET """,
"""   Q [""",
"""M """
  ]
  Fields = [
    """({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2}((\+|\-)\d\d:\d\d)? (am|AM|pm|PM))\s+\S+\s+PACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\S+\s+Q\s+\[(\s|({dns_query_flags}.+?))\s+\S+\]\s+({dns_query_type}\S+)\s+({dns_query}.+?)\s*(\s\w+=|$|<)""",
    """<Identifier>\S+\s+({host}\S+?)<\/Identifier>"""
  ]


}
```