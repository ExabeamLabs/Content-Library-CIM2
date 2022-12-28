#### Parser Content
```Java
{
Name = sophos-ep-kv-network-traffic-fail-blocked-1
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::WindowsFirewall::Blocked"""" ]
  Fields = [
    """\s({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """host="({host}[^"]+)""",
    """alert_id="({event_code}[^"]+)"""",
    """user="({user}[^"]+)""",
    """src_ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """rule_name="({rule}[^"]+)""",
    """alert_type="({event_name}[^"]+)"""",
    """rule_reason="({additional_info}[^"]+)\s*"""",
    """Event::Endpoint::WindowsFirewall::({action}Blocked)""",
  ]
  DupFields = [ "host->src_host" ]


}
```