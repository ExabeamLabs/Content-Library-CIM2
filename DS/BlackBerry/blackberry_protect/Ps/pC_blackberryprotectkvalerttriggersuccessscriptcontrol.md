#### Parser Content
```Java
{
Name = "blackberry-protect-kv-alert-trigger-success-scriptcontrol"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS","yyyy-MM-dd HH:mm:ss.SSS","MMM dd HH:mm:ss"]
Conditions = [
"""CylancePROTECT"""
"""Event Type: ScriptControl"""
"""Interpreter: """
]
Fields = [
"""\[({host}[\w\-.]+)\]\s*Event Type:"""
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{3})\d+"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})\d+"""
"""({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)"""
"""Event Type:\s*({alert_type}[^,]+)\s*,"""
"""Event Name:\s*({additional_info}[^,]+)\s*,"""
"""Device Name:\s*({src_host}[^,]+)\s*,"""
"""File Path:\s*({malware_url}[^,]+)\s*,"""
"""Interpreter:\s*({alert_name}[^,]+)\s*,"""
"""User Name:\s*(?:SYSTEM|({user}[\w\.\-]{1,40}\$?))\s*(,|$)"""
]
DupFields = [
"malware_url->malware_file_name"
]
ParserVersion = "v1.0.0"


}
```