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
    """sourceip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventType":"({alert_type}[^"]+)""",
    """PolicyName":"({policy_name}[^"]+)""",
    """RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """RuleName":"({rule}[^"]+)""",
    """ImageFileName":"({file_path}[^"]+)"+,""",
    """CommandLine":"({process_command_line}[^"]+)"+,""",
   ]


}
```