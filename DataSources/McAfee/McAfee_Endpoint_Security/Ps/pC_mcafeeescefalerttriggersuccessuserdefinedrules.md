#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-userdefinedrules
  ParserVersion = v1.0.0
  Product = McAfee Endpoint Security
  Conditions = [ """CEF""","""|McAfee|ePolicy Orchestrator|""", """User-defined Rules:""" ]

cef-mcafee-epo-alert = {
  Vendor = McAfee
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=(?:0.0.0.0|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """\sfname=({url}.+?)\s+(\w+=)""",
    """\sfname=({url}[^=]+?\\+({malware_file_name}[^\\=]+?))\s+\w+=""",
    """\sduser=(SYSTEM|N\/A|(({domain}[^=\\]+)\\+)?({user}.+?))\s+(\w+=|$)""",
    """\sdntdom=(?:\(none\)|({domain}[^\s]+))""",
    """\seventId=({alert_id}\d+)""",
    """\sexternalId=({alert_id}\d+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^.|]+)""",
    """\scs1=(?:none|({alert_name}.+?))\s+(\w+=|$)""",
    """\scat=({threat_category}.+?)\s+(\w+=|$)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^.|]+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^\|]+)""",
    """\scategoryOutcome=/?({result}.+?)\s+(\w+=|$)""",
  ]
  DupFields = ["malware_file_name->file_name"
}
```