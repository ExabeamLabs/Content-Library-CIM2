#### Parser Content
```Java
{
Name = infoblox-bddi-str-dns-request-successresolving
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]: success resolving """, """ (in """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """]: success resolving '({dns_query}[^'\/]+?)\/({dns_query_type}[^']+)' \(in '(\.|({result}[^']+))'"""
  ]


}
```