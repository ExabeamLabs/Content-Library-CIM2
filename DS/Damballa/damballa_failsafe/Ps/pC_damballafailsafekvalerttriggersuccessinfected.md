#### Parser Content
```Java
{
Name = damballa-failsafe-kv-alert-trigger-success-infected
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Damballa Failsafe
  TimeFormat = "epoch"
  Conditions = [ """Damballa|Failsafe|""", """msg=infected""" ]
  Fields = [
    """\|start=({time}\d{13})""",
    """\s+({host}[^\s]+)\s+Failsafe\s+\d+""",
    """Damballa\|Failsafe\|[^|]+?\|({alert_name}[^|]+)\|""",
    """Damballa\|Failsafe\|[^|]+?\|({alert_type}[^|]+)\|""",
    """\|cs2=({alert_type}[^|]+)""",
    """\|msg=({alert_name}[^|]+)""",
    """\|cfp1=({alert_severity}[^\|]+)""",
    """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|shost=(?:((\d+\.){3}\d+)|({src_host}[^\|]+))""",
    """\|cs6=({alert_id}[^\|]+)"""
  ]


}
```