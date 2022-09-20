#### Parser Content
```Java
{
Name = bluecatnetworks-adonis-leef-dns-request-success-bcn
Vendor = BlueCat Networks
Product = BlueCat Networks Adonis
TimeFormat = "epoch"
Conditions = [
  """LEEF"""
  """|DNS_Query|"""
  """|BCN|"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
  """\|cat=({dns_query_type}[^\s_]+)"""
  """src=({src_ip}[\da-fA-F\.:]+)"""
  """url=\s*({query}[^\s"]+)"?""",
]
ParserVersion = "v1.0.0"


}
```