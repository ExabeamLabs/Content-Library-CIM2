#### Parser Content
```Java
{
Name = "netwrix-auditor-kv-app-activity-success-vmware"
Vendor = "Netwrix"
Product = "Netwrix Auditor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""DataSource : VMware"""
"""Action :"""
"""Where :"""
"""Who :"""
]
Fields = [
"""When\s*:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""
"""\sMessage:\s*({operation}[^:]+?)\s*\w+\s*:"""
"""Who\s*:\s*(({domain}[^\\\s]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Where\s*:\s*(\w+:\/+)({dest_host}[\w\-.]+)"""
"""ObjectType\s*:\s*({additional_info}.+?)\s*\w+\s*:"""
"""What\s*:\s*({resource}.+?)({object}[^\\]+?)\s+When\s*:"""
"""({app}VMware)"""
]
ParserVersion = "v1.0.0"


}
```