#### Parser Content
```Java
{
Name = mcafee-es-cef-app-activity-ops
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|McAfee|ePolicy Orchestrator|""", """cat=ops.""" ]

cef-mcafee-epo-system-info = {
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=(?:0.0.0.0|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """\sfname=({malware_url}.+?)\s+(\w+=)""",
    """\sfname=({malware_url}[^=]+?\\+({malware_file_name}[^\\=]+?))\s+(cs1=)""",
    """\sduser=(SYSTEM|N\/A|(({domain}[^=\\]+)\\+)?({user}.+?))\s+(\w+=|$)""",
    """\sdntdom=(?:\(none\)|({domain}[^\s]+))""",
    """\seventId=({alert_id}\d+)""",
    """\sexternalId=({alert_id}\d+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^.|]+)""",
    """\scs1=(?:none|({event_name}.+?))\s+(\w+=|$)""",
    """\scat=({threat_category}.+?)\s+(\w+=|$)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^.|]+)""",
    """\|McAfee\|ePolicy[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^\|]+)"""
  
}
```