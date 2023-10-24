#### Parser Content
```Java
{
Name = cisco-fp-kv-dns-response-success-dnsquery
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """AccessControlRuleAction: """, """ApplicationProtocol: DNS""", """DNSQuery: """ ]
  Fields = [
    """\w+\s+\d+ \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s*""",
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """SrcPort:\s*({src_port}\d+)""",
    """DstPort:\s*({dest_port}\d+)""",
    """AccessControlRuleAction:\s*({result}[^,]+)""",
    """Protocol:\s*({protocol}[^,]+)""",
    """User:\s*(Unknown|Not Found|No Authentication Required|({user}[\w\.\-]{1,40}\$?)),""",
    """InitiatorBytes:\s*({bytes_out}\d+)""",
    """ResponderBytes:\s*({bytes_in}\d+)""",
    """ACPolicy:\s*({policy_name}[^,]+)""",
    """DNSQuery:\s*({dns_query}[^,]+)""",
    """DNSRecordType:\s*({dns_query_type}[^:,]+?),""",
    """IngressInterface: ({src_interface}[^\s,]+?),""",
    """EgressInterface: ({dest_interface}[^\s,]+?),""",
    """\WDNSResponseType:\s*({dns_response}[^,]+)"""
]


}
```