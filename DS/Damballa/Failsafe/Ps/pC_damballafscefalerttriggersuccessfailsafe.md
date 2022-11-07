#### Parser Content
```Java
{
Name = damballa-fs-cef-alert-trigger-success-failsafe
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Failsafe
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Damballa|Failsafe""" ]
  Fields = [
    """\|Damballa\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^\|]+?)\|""",
    """\|Damballa\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^\|]+)""",
    """\seventId=({alert_id}[^\s]+)""",
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}[^\.\s]+)""",
    """\sdhost=({dest_host}[^\.\s]+)""",
    """\srequest=({url}.+?)\s+\w+=""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sreason=({alert_type}[^\s]+)"""
  ]


}
```