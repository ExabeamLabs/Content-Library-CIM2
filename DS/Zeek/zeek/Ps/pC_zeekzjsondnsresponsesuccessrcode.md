#### Parser Content
```Java
{
Name = zeek-z-json-dns-response-success-rcode
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""""id.orig_h"""
""""id.resp_h"""
""""rcode"""
""""rcode_name"""
]
  Fields = [
    """\"_system_name\":\"({host}[^\"]+)""",
    """\"ts\"+:\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """\"uid\"+:\"+({connection_id}[^\"]+)""",
    """\"id\.orig_h\"+:\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\"id\.orig_p\"+:({src_port}\d+)""",
    """\"id\.resp_h\"+:\"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\"id\.resp_p\"+:({dest_port}\d+)""",
    """\"proto\"+:\"+({protocol}[^\"]+)""",
    """\"query\"+:\"+({dns_query}[^\"]+)""",
    """"qtype_name\"+:\"+({dns_query_type}[^\"]+)""",
    """\"rcode_name\"+:\"+({dns_response_code}[^\"]+)""",
    """\"answers\"+:\[({dns_response}.+?)\]""",
    """\"rejected\"+:({result}\w+)"""
  ]


}
```