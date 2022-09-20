#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-epolicyorchestrator
  Product = McAfee Endpoint Security
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|McAfee|ePolicy Orchestrator|""", """Access Protection rule violation detected and """ ]
  Fields = ${McAfeeParsersTemplates.cef-mcafee-epo-alert.Fields}[
    """Access Protection rule violation detected and ({action}(NOT )?blocked)""",
    """\sshost=(_|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\ssrc=({dest_ip}[a-fA-F\d.:]+)""",
    """\ssproc=({process_path}({process_dir}[^=]*?[\\\/]+)?({process_name}[^=\\\/]+))(\s+\w+=|\s*$)""",
  ]

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