#### Parser Content
```Java
{
Name = mcafee-es-cef-alert-trigger-success-epolicyorchestrator
  Product = McAfee Endpoint Security
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|McAfee|ePolicy Orchestrator|""", """Access Protection rule violation detected and """ ]
  Fields = ${McAfeeParsersTemplates.cef-mcafee-epo-alert.Fields}[
    """Access Protection rule violation detected and ({result}(NOT )?blocked)""",
    """\sshost=(_|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssproc=({process_path}({process_dir}[^=]*?[\\\/]+)?({process_name}[^=\\\/]+))(\s+\w+=|\s*$)""",
  ]

cef-mcafee-epo-alert = {
  Vendor = McAfee
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdst=(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\sfname=({malware_url}.+?)\s+(\w+=)""",
    """\sfname=({malware_url}[^=]+?\\+({malware_file_name}[^\\=]+?))\s+\w+=""",
    """\sduser=(SYSTEM|N\/A|(({domain}[^=\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
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