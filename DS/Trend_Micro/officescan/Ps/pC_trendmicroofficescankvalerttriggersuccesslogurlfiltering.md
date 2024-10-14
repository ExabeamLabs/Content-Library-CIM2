#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-logurlfiltering"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" WFBSS-SVC-AC [LogUrlFiltering"""
]
Fields = [
"""({host}\S+) WFBSS-SVC-AC"""
"""\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d) \d+\.\d+\.\d+\.\d+"""
"""Device name="({src_host}[^"]+)"""
"""User="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""URL="({malware_url}[^"]+)"""
"""\[({alert_type}[^@]+)"""
]
DupFields = [
"alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```