#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-logbehavior"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" WFBSS-SVC-AC [LogBehaviorMonitoring"""
"""Security Threat=""""
]
Fields = [
"""({host}\S+) WFBSS-SVC-AC"""
"""\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d) \d+\.\d+\.\d+\.\d+"""
"""Device name="({src_host}[^"]+)"""
"""User="({user}[\w\.\-]{1,40}\$?)"""
"""Security Threat="({alert_name}[^"]+)"""
"""Subject="({process_path}({process_dir}[^"]+)\\({process_name}[^"]+))""""
"""\[({alert_type}[^@]+)"""
]
ParserVersion = "v1.0.0"


}
```