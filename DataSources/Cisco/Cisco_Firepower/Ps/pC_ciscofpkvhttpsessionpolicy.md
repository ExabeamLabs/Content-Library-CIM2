#### Parser Content
```Java
{
Name = cisco-fp-kv-http-session-policy
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """Policy: """, """ApplicationProtocol: HTTP""" ]
  Fields = [
    """\w+\s+\d+ \d\d:\d\d:\d\d ({host}[\w.\-]+)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s+(\(|\%)""",
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """SrcIP:\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """DstIP:\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """DstIP:\s+({web_domain}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """SrcPort:\s+({src_port}\d+)""",
    """DstPort:\s+({dest_port}\d+)""",
    """AccessControlRuleAction:\s+({action}[^,]+)""",
    """User:\s+(Unknown|No Authentication Required|({user}[^,\s]+))""",
    """UserAgent:\s+({user_agent}.+?),\s+Client:""",
    """Protocol:\s+({protocol}[^,]+)""",
    """InitiatorBytes:\s+({bytes_out}\d+)""",
    """ResponderBytes:\s+({bytes_in}\d+)""",
    """URLCategory:\s+({categories}({category}[^,;]+)[^,]+)""",
    """URL:\s+({url}\S+?)(,\s+\w+:|\s)""",
    """URL:\s+(?:-|\w+:\/+)({web_domain}[^\s\/:]+)""",
    """URL:\s+(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """URL:\s+.*?({uri_query}\?[^\s"]+)""",
    """IngressInterface: ({src_interface}[^\s,]+?),""",
    """EgressInterface: ({dest_interface}[^\s,]+?),""",
    """Priority: ({priority}\d+),""",
    """AccessControlRuleName: ({rule}[^,]+),""",
    """ApplicationProtocol: ({app_protocol}[^,]+),""",
    """IntrusionPolicy: ({alert_name}[^,]+),"""
  ]


}
```