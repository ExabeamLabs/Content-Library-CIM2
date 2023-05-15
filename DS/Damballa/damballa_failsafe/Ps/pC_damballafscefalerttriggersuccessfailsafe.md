#### Parser Content
```Java
{
Name = damballa-fs-cef-alert-trigger-success-failsafe
  ParserVersion = v1.0.0
  Vendor = Damballa
  Product = Damballa Failsafe
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Damballa|Failsafe""" ]
  Fields = [
    """\|Damballa\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^\|]+?)\|""",
    """\|Damballa\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^\|]+)""",
    """\seventId=({alert_id}[^\s]+)""",
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sshost=({src_host}[^\.\s]+)""",
    """\sdhost=({dest_host}[^\.\s]+)""",
    """\srequest=({malware_url}.+?)\s+\w+=""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sreason=({alert_type}[^\s]+)"""
  ]


}
```