#### Parser Content
```Java
{
Name = bluecatnetworks-bnetworks-leef-dns-request-success-bcn
Vendor = BlueCat Networks
Product = BlueCat Networks
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """LEEF"""
  """|DNS_Query|"""
  """|BCN|"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """\|cat=({dns_query_type}[^\s_]+)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """url=\s*({dns_query}[^\s"]+)"?""",
]
ParserVersion = "v1.0.0"


}
```