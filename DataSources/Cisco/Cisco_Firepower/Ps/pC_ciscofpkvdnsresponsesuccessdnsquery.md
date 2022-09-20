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
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s*(\(|\%)""",
    """SrcIP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """DstIP:\s*({dest_ip}[A-Fa-f:\d.]+)""",
    """SrcPort:\s*({src_port}\d+)""",
    """DstPort:\s*({dest_port}\d+)""",
    """AccessControlRuleAction:\s*({action}[^,]+)""",
    """Protocol:\s*({protocol}[^,]+)""",
    """User:\s*(Unknown|Not Found|No Authentication Required|({user}[^,]+)),""",
    """InitiatorBytes:\s*({bytes_out}\d+)""",
    """ResponderBytes:\s*({bytes_in}\d+)""",
    """ACPolicy:\s*({policy_name}[^,]+)""",
    """DNSQuery:\s*({dns_query}[^,]+)""",
    """DNSRecordType:\s*({dns_query_type}[^:,]+?),""",
    """IngressInterface: ({src_interface}[^\s,]+?),""",
    """EgressInterface: ({dest_interface}[^\s,]+?),"""
]


}
```