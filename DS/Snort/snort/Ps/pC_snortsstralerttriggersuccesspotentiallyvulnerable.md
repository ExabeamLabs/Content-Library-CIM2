#### Parser Content
```Java
{
Name = "snort-s-str-alert-trigger-success-potentiallyvulnerable"
Vendor = "Snort"
Product = "Snort"
TimeFormat = "MMM dd HH:mm:ss yyyy z"
Conditions = [
"""[Classification:"""
"""[Priority:"""
"""[Impact:"""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s\w+:"""
""":\s({time}(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\d\d\s\d\d:\d\d:\d\d)"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+\s+\d+\s+\d\d:\s*\d\d\s*:\d\d \d+ \w+)"""
"""\[\s*({alert_name}\d+:\d+:\d+)\]"""
"""\[Classification:\s*({alert_type}[^\]]+)\]"""
"""\[Priority:\s*({alert_severity}\d+)\]"""
"""CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
"""\[\s*\d+:\d+:\d+\]\s+"({additional_info}[\w\-.]+\s+({alert_name}[^"]+))""""
""" From \"(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\"\s]+))"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\{\w+\}\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s\((unknown|({src_country}[^\)]+))\)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""->\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\((unknown|({dest_country}[^\)]+))\)"""
"""\[Impact:\s*(Unknown|({impact}[^\]]+))"""
]
ParserVersion = "v1.0.0"


}
```