#### Parser Content
```Java
{
Name = mcafee-epo-kv-alert-trigger-success-string
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = Mcafee EPO
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """:epoEventEventDesc: 'STRING:""", """:epoEventThreatCategory: 'STRING:""", """:epoEventThreatActionTaken: 'STRING:""" ]
  Fields = [
    """\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S*\s+({host}[\w\-.]+)\s+\w+""",
    """:epoEventEventDesc:\s*'STRING:\s*\\?"({alert_name}[^"]+?)\\?"""",
    """:epoEventTargetIPV6:\s*'STRING:\s*\\?"({dest_ip}[A-Fa-f:\d.]+)""",
    """:epoEventTargetProcessName:\s*'STRING:\s*\\?"({process_path}(({process_dir}[^"]*?)\\)?({process_name}[^"\\]*?))\\?"""",
    """:epoEventTargetFileName:\s*'STRING:\s*\\?"(|({file_path}(|({file_dir}[^"]*?))[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?)))\\?"""",
    """:epoEventTargetUserName:\s*'STRING:\s*\\?"(({domain}[^\\\s"']+)\\+)?(SYSTEM|({user}[^\\\s"']+))\\?"""",
    """:epoEventThreatCategory:\s*'STRING:\s*\\?"({alert_type}[^"]+?)\\?"""",
    """:epoEventThreatSeverity:\s*'STRING:\s*\\?"({alert_severity}[^"']+?)\\?"""",
    """:epoEventThreatActionTaken:\s*'STRING:\s*\\?"(None|({action}[^"']+?))\\?"""",
    """:epoEventOsType:\s*'STRING:\s*\\?"({os}[^"']+?)\\?""""
  ]
  DupFields = [ "alert_type->threat_category" ]


}
```