#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-notauthorized
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Conditions = [ """CEF""","""|McAfee|ePolicy Orchestrator|""", """The user was not authorized to access the requested URL""" ]
  Fields = [
    
    """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=(?:0.0.0.0|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """\sfname=({malware_url}.+?)\s+(\w+=)""",
    """\sfname=({malware_url}[^=]+?\\+({malware_file_name}[^\\=]+?))\s+\w+=""",
    """\sduser=(SYSTEM|N\/A|(({domain}[^=\\]+)\\+)?({user}.+?))\s+(\w+=|$)""",
    """\sdntdom=(?:\(none\)|({domain}[^\s]+))""",
    """\seventId=({alert_id}\d+)""",
    """\sexternalId=({alert_id}\d+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^.|]+)""",
    """\scs1=(?:none|({alert_name}.+?))\s+(\w+=|$)""",
    """\scat=({threat_category}.+?)\s+(\w+=|$)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^.|]+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^\|]+)""",
    """\scategoryOutcome=/?({action}.+?)\s+(\w+=|$)""",
    """\ssuser=({user}.+?)\s+(\w+=|$)""",
    """\scatdt=({alert_type}.*?)\s+(\w+=|$)""",
  ]
  DupFields = ["malware_file_name->file_name"]
  ParserVersion = "v1.0.0"


}
```