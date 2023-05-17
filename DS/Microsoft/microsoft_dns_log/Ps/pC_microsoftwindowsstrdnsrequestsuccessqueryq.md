#### Parser Content
```Java
{
Name = microsoft-windows-str-dns-request-success-queryq
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft DNS Log
  TimeFormat = "dd.MM.yyyy HH.mm.ss"
  Conditions = [
""" PACKET """,
"""   Q ["""
  ]
  Fields = [
    """({time}\d+\/\d+\/\d\d\d\d \d{1,2}:\d{1,2}:\d{1,2})\s+\S+\s+PACKET\s""",
    """({time}\d{1,2}.\d{1,2}\.\d{1,4} \d{1,2}\.\d{1,2}\.\d{1,2})\s\w+\sPACKET\s""",
    """\sPACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\S+\s+Q\s+\[\S+\s+(\s|({dns_query_flags}[^\s]+))\s+\S+\]\s+({dns_query_type}\S+)\s+({dns_query}[^\",\s]+)\"*"""
  ]


}
```