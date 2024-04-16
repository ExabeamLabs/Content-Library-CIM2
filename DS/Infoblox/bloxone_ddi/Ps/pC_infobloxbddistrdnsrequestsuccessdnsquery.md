#### Parser Content
```Java
{
Name = "infoblox-bddi-str-dns-request-success-dnsquery"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = [ "dd-MMM-yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss" ]
Conditions = [
""": query: """
"""named"""
]
Fields = [
  """\d\d:\d\d:\d\d(\.\d+Z)? (::ffff:)?({host}\S+)""",
  """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)""",
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
  """\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))#({src_port}\d+)(?:)""",
  """query:\s*({dns_query}\S+)\s"""
  """\sIN\s({dns_query_type}\w{1,5})\s""",
  """\s+IN\s.+?\s+({dns_query_flags}[^\d\w].*?)\s""",
  """response:\s*({dns_response_code}[^\s]+)\s""",
  """\sIN\s+.+?\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(;|$|"|\.|\))""",
  """ CNAME ({additional_info}[^;]+?)\.?;""",
  ]
ParserVersion = "v1.0.0"


}
```