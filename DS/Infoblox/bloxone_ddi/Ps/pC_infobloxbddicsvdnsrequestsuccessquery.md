#### Parser Content
```Java
{
Name = infoblox-bddi-csv-dns-request-success-query
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "epoch_sec"
  Conditions = [ """,Query,""" ]
  Fields = [
    """({time}\d{10}),[^,]*.Query,""",
    """,Query,(|({protocol}[^,]+)),""",
    """,Query,([^,]*,)({src_ip}[a-fA-F\d:\.]+),""",
    """,Query,([^,]*,){2}({src_port}\d{1,5}),""",
    """,Query,([^,]*,){5}({dns_query}[^,]+),""",
    """,Query,([^,]*,){7}({dns_query_type}[^,]+),"""
  ]
  ParserVersion = "v1.0.0"


}
```