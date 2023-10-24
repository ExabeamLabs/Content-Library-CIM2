#### Parser Content
```Java
{
Name = "extrahop-revealx-json-dns-request-success-dnsquery"
Vendor = "Extrahop"
Product = "Extrahop Reveal(x)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""opcode":"QUERY"""
"""vendor":"ExtraHop"""
"""qname"""
"""qtype"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[^\s]+)""",
  """"proto":"({protocol}[^"]+)""",
  """"clientAddr":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"serverAddr":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"clientPort":({src_port}\d+)""",
  """"serverPort":({dest_port}\d+)""",
  """"qname":"({dns_query}[^"]+)""",
  """"qtype":"({dns_query_type}[^"]+)""",
  """"error":"({error_code}[^"]+)""",
  """"rspBytes":({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```