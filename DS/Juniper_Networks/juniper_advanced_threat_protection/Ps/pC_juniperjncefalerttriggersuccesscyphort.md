#### Parser Content
```Java
{
Name = juniper-jn-cef-alert-trigger-success-cyphort
  Vendor = Juniper Networks
  Product = Juniper Advanced Threat Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""|Cyphort|Cortex|"""]
  Fields = [
    """lastActivityTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|""",
    """\seventId=({alert_id}\d+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sfileName =({file_name}.+?)\s+\w+=""",
    """\surl=({url}[^\r\n]+)\s+""",
    """\smalwareSeverity=({alert_severity}.+?)\s+\w+=""",
    """\smalwareCategory=({alert_type}.+?)\s+\w+="""
  ]
  DupFields = ["file_name->process_name"]
  ParserVersion = "v1.0.0"


}
```