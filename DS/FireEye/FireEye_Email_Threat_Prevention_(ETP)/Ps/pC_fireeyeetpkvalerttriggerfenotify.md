#### Parser Content
```Java
{
Name = fireeye-etp-kv-alert-trigger-fenotify
  ParserVersion = v1.0.0
  Vendor = FireEye
  Product = FireEye Email Threat Prevention (ETP)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """alert (id:""", """mvx-status:""", """fenotify-""", """alert-url:""", """sig-name:""" ]
  Fields = [
    """appliance:\s*({host}[^\s]+)""",
    """occurred:\s*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """\salert\s*\(id:({alert_id}[^,]+),\s*name:({alert_type}[^\s]+)\s+severity:({alert_severity}[^\s]+)""",
    """sig-name:({alert_name}[^:]+?)\s+\S+:""",
    """src:.+?ip:\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """dst:.+?ip:\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """alert-url:\s+({malware_url}[^\s]+)"""
  ]


}
```