#### Parser Content
```Java
{
Name = microsoft-windows-str-dns-request-success-packetn
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [
""" PACKET """,
"""   N ["""
  ]
  Fields = [
    """({time}\d{1,2}\/\d{1,2}\/\d{4} \d{1,2}:\d{1,2}:\d{1,2} (am|AM|pm|PM))\s+\S+\s+PACKET\s""",
    """\sPACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}[A-Fa-f\d:.]+)\s+\S+\s+N\s+\[\S+\s+({dns_query_flags}\S+)?\s+\S+\]\s+({dns_query_type}\S+)\s+({dns_query}.+$)"""
  ]


}
```