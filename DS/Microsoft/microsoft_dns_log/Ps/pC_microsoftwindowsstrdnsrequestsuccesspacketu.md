#### Parser Content
```Java
{
Name = microsoft-windows-str-dns-request-success-packetu
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft DNS Log
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a", "MM/dd/yyyy HH:mm:ss"]
  Conditions = [ 
""" PACKET """,
"""   U ["""
  ]
  Fields = [
    """({time}\d{1,2}\/\d{1,2}\/\d{4} \d{1,2}:\d{1,2}:\d{1,2})\s*(am|AM|pm|PM)?\s+\S+\s+PACKET\s""",
    """\sPACKET\s+\S+\s+({protocol}\S+)\s+({operation}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\S+\s+U\s+\[({dns_query_flags}\S+)?\s+\S+\]\s+({dns_query_type}\S+)\s+({dns_query}.+?)\s*(\s\w+=|$|<|")""",
  ]


}
```