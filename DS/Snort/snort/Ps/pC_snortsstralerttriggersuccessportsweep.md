#### Parser Content
```Java
{
Name = "snort-s-str-alert-trigger-success-portsweep"
Vendor = "Snort"
Product = "Snort"
TimeFormat = "MMM dd HH:mm:ss"
Conditions = [
"""[Classification:"""
"""[Priority:"""
"""snort["""
]
Fields = [
"""({time}\w+\s+\d+\s\d\d:\d\d:\d\d)\s\S+\ssnort\["""
"""\s({host}[^\s]+)\s+snort\["""
"""\}\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?\s+->\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?"""
"""\[Classification:\s+({alert_type}[^\]]+)"""
"""\[Priority:\s+({alert_severity}[^\]]+)"""
"""\d+\](\s\([^\)]+\))?\s({alert_name}.+?)\s*\[Classification"""
"""snort\[({event_code}\d+)"""
"""Priority:.+?\{(PROTO:)?({protocol}[^\}]+)\}"""
]
ParserVersion = "v1.0.0"


}
```