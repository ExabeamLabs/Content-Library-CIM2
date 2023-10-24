#### Parser Content
```Java
{
Name = "algosec-fa-cef-alert-trigger-success-unauthorizedtraffic"
Product = "AlgoSec Firewall Analyzer"
Vendor = "AlgoSec"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|AlgoSec|Firewall Analyzer|"""
"""Unauthorized traffic"""
]
Fields = [
"""({host}[^\s]+)\s+:\s+CEF"""
"""CEF:\d+\|([^\|]+\|){2}({version}[^\|]+)"""
"""CEF:\d+\|([^\|]+\|){3}({alert_type}[^\|]+)"""
"""({alert_name}Unauthorized traffic)"""
"""msg=Summary:\s+\w+\s*({alert_severity}\d+)"""
"""Unauthorized traffic from\s+({src_network}.+?)\s+to\s+({dest_network}[^\s]+)\s+"""
]
ParserVersion = "v1.0.0"


}
```