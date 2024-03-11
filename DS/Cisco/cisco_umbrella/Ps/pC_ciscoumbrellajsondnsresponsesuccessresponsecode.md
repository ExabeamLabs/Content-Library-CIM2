#### Parser Content
```Java
{
Name = cisco-umbrella-json-dns-response-success-responsecode
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,EventType":"""", """,Identities":"""", """,ResponseCode":"""", """,BlockedCategories":"""",""",QueryType":"""" ]
  Fields = [
    """,Timestamp":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """,Identities":"({identities}[^,]+),""",
    """,InternalIp":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,""",
    """,ExternalIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """,Action":"({result}[^,]+),""",
    """,QueryType":"({dns_query_type}[^,]+),""",
    """,ResponseCode":"({dns_response_code}[^,]+),""",
    """,Domain":"({dns_query}[^,]+),""",
    """,Categories":"({categories}({category}[^,"]+)[^"]*),"""
  ]
  ParserVersion = "v1.0.0"


}
```