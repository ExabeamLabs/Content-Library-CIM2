#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-logvirus"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" WFBSS-SVC-AC [LogVirus"""
"""Virus/Malware Name =""""
]
Fields = [
"""({host}\S+) WFBSS-SVC-AC"""
"""\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d) \d+\.\d+\.\d+\.\d+"""
"""Device name="({src_host}[^"]+)"""
"""User="({user}[\w\.\-]{1,40}\$?)"""
"""Virus\/Malware Name ="({alert_name}[^"]+)"""
"""File name="({file_name}[^"]+)"""
"""\[({alert_type}[^@]+)"""
]
ParserVersion = "v1.0.0"


}
```