#### Parser Content
```Java
{
Name = damballa-failsafe-kv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Damballa Failsafe
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Damballa|Failsafe|""", """message:"""  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\|dvchost=({host}[^\|]+)""",
    """\sDamballa\|Failsafe\|[^\|]+\|({alert_name}[^\|]+)""",
    """\|cs2=({alert_name}[^\|]+)""",
    """\|cfp1=({alert_severity}[^\|]+)""",
    """\|cs7=({alert_type}[^\|]+)""",
    """\|destinationDnsDomain=({url}[^\|]+)""",
    """\|dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\|externalId=({alert_id}[^\|]+)""",
    """\|shost=({src_host}[^\|]+)""",
    """\|src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```