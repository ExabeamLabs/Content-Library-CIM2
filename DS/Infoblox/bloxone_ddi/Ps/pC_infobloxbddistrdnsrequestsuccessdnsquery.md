#### Parser Content
```Java
{
Name = "infoblox-bddi-str-dns-request-success-dnsquery"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
Conditions = [
""": query: """
"""named["""
]
Fields = [
  """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)""",
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
  """client\s*(::ffff:)?({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})#({src_port}\d+)(?:)""",
  """query:\s*({dns_query}\S+)\s"""
  """\sIN\s({dns_query_type}\w{1,5})\s""",
  """\s+IN\s.+?\s+({dns_query_flags}[^\d\w].*?)\s""",
  """response:\s*({dns_response_code}[^\s]+)\s""",
  """IN\s*.+?s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """ CNAME ({cname}[^;]+?)\.?;""",
]
ParserVersion = "v1.0.0"


}
```