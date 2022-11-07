#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-activity-success-sourceip
  Vendor = CrowdStrike
  ParserVersion = v1.0.0
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ CrowdStrike """, """ AuditLog """, """sourceip=""", """"eventType":"""  ]
  Fields = [
    """HostName":"({host}[^"]+)"""",
    """\s({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)""",
    """({operation}CrowdStrike mule_ee AuditLog)""",
    """sourceip="({src_ip}[a-fA-F\d\.:]+)""",
    """EventType":"({alert_type}[^"]+)""",
    """PolicyName":"({policy_name}[^"]+)""",
    """RemoteAddress":"({dest_ip}[a-fA-F\d\.:]+)""",
    """RuleName":"({rule}[^"]+)""",
    """ImageFileName":"({file_path}[^"]+)"+,""",
    """CommandLine":"({process_command_line}[^"]+)"+,""",
   ]


}
```