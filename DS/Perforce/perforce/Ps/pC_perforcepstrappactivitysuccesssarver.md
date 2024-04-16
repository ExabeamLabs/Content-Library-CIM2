#### Parser Content
```Java
{
Name = "perforce-p-str-app-activity-success-sarver"
Vendor = "Perforce"
Product = "Perforce"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
"""Perforce server"""
""" info:"""
]
Fields = [
"""({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
"""\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d\spid ({process_id}\d+) (({user}[\w\.\-]{1,40}\$?)@)?({additional_info}[^\s]+)"""
"""\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\/)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s"""
"""\]\s+'({operation}[^\s\']+)"""
"""\s+({object}\/+[^\/\s'@\.]+(\/+[^\/\s'@\.]+)?)?\s*(|({resource}[^'\s\-]+?))'\s*$"""
"""\/\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\s({operation}[^\[\]']+?)\s\/\/"""
]
ParserVersion = "v1.0.0"


}
```