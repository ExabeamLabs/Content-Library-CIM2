#### Parser Content
```Java
{
Name = "commvault-threatwise-str-alert-trigger-success-synscan"
  Vendor = "Commvault"
  Product = "Commvault ThreatWise"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ traps[""",  """: SYN SCAN :""" ]
Fields = [
  """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)""",
  """\d{2}:\d{2}:\d{2} ({host}[\w\-.]+)\s+""",
  """({event_category}traps)\[({session_id}\d+)\]({protocol}.+?)\s+\:\s+({alert_name}SYN SCAN)\s+\:\s+({event_name}Scan)\s+\:\s+({interface}.+?)\s+\:\s+({os}.+?)\s+\:\s+\d+\|({additional_info}.+?)\s*:\s*\d+(?:\.\d+)?$""",
  """({event_category}traps)\[({session_id}\d+)\]({protocol}.+?)\s\:\s+({alert_name}SYN SCAN)\s+\:\s+\d+\.\d+\s+\:""",
  """\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\s+:\s+({src_port}\d+))\s+\:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\s+:\s+({dest_port}\d+))\s+\:\s+({interface}.+?)\s+\:\s+({os}.+?)\s+\:\s+\d+"""
]
ParserVersion = "v1.0.0"


}
```