#### Parser Content
```Java
{
Name = infoblox-bddi-csv-dns-response-success-response
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "epoch_sec"
  Conditions = [ """,Response,""" ]
  Fields = [
    """({time}\d{10}),[^,]*,Response,""",
    """,Response,(|({protocol}[^,]+)),""",
    """,Response,([^,]*,)({src_ip}[a-fA-F\d:\.]+),""",
    """,Response,([^,]*,){2}({src_port}\d{1,5}),""",
    """,Response,([^,]*,){5}({dns_query}[^,]+),""",
    """,Response,([^,]*,){7}({dns_query_type}[^,]+),""",
    """,Response,([^,]*,){9}({dns_response_code}[^,]+),""",
    """,Response,([^,]*,){9}[^\n]+?({dest_ip}(\d{1,3}\.){3}\d{1,3})"""
  ]
  ParserVersion = "v1.0.0"


}
```