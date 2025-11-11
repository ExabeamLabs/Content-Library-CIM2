#### Parser Content
```Java
{
Name = infoblox-bddi-mix-dns-response-success-opcode_query
    Vendor = Infoblox
    Product = BloxOne DDI
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """opcode: QUERY""", """named:""", """QUESTION SECTION:""", """AUTHORITY SECTION:""", """ANSWER SECTION:""" ]
    Fields = [
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s\S+\sdns\[\d+\]:""",
      """\s({host}[\w\-\.]+)\sdns\[\d+\]:""",
      """({protocol}dns)""",
      """\snamed:[^"]*?\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#({src_port}\d+))?;\s\snamed:""",
      """\sstatus:\s*({dns_response_code}[^,]+),""",
      """QUESTION SECTION:;\s*({dns_query}[^\s;]+?)\.\s+\w+\s+\w+;""",
      """QUESTION SECTION:;\s*\S+\s*({dns_query_flags}\w+)\s+\w+;""",
      """QUESTION SECTION:;(\s*\S+\s*){2}({dns_query_type}\w+);""",
      """ANSWER SECTION:\s*({dns_response}[^"]+?)AUTHORITY SECTION:"""
    ]
    ParserVersion = "v1.0.0"
  

}
```