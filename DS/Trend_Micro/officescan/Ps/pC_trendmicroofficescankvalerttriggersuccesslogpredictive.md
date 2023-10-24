#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-logpredictive"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" WFBSS-SVC-AC [LogPredictiveMachineLearning"""
]
Fields = [
"""({host}\S+) WFBSS-SVC-AC"""
"""\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d) \d+\.\d+\.\d+\.\d+"""
"""Device name="({src_host}[^"]+)"""
"""User="({user}[\w\.\-]{1,40}\$?)"""
"""Unknown Threat="({alert_name}[^"]+)"""
"""File name="({file_name}[^"]+)"""
"""\[({alert_type}[^@]+)"""
]
ParserVersion = "v1.0.0"


}
```