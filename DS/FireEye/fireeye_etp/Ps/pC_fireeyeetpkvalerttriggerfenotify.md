#### Parser Content
```Java
{
Name = fireeye-etp-kv-alert-trigger-fenotify
  ParserVersion = v1.0.0
  Vendor = FireEye
  Product = FireEye ETP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """alert (id:""", """mvx-status:""", """fenotify-""", """alert-url:""", """sig-name:""" ]
  Fields = [
    """appliance:\s*({host}[^\s]+)""",
    """occurred:\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """\salert\s*\(id:({alert_id}[^,]+),\s*name:({alert_type}[^\s]+)\s+severity:({alert_severity}[^\s]+)""",
    """sig-name:({alert_name}[^:]+?)\s+\S+:""",
    """src:.+?ip:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst:.+?ip:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """alert-url:\s+({malware_url}[^\s]+)"""
  ]


}
```