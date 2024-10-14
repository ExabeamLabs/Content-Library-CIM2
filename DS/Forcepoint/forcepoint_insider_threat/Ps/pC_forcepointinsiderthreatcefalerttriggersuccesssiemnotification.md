#### Parser Content
```Java
{
Name = "forcepoint-insiderthreat-cef-alert-trigger-success-siemnotification"
Vendor = "Forcepoint"
Product = "Forcepoint Insider Threat"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|SIEM Notification|"""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF:"""
"""\|SIEM Notification\|(?:[^\|]+\|){10}\s+((NT AUTHORITY|({domain}[^\/\s]+))\/)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\|"""
"""SIEM Notification\|(?:[^\|]+\|){7}\s+([^\\]*\\)?({src_host}[^\s\|\$]+)\$?\s*"""
"""SIEM Notification\|(?:[^\|]+\|){3}\s+({alert_name}[^\|]+)\s+\|"""
"""SIEM Notification\|(?:[^\|]+\|){4}\s+({alert_type}[^\|]+)\s+\|"""
"""SIEM Notification\|(?:[^\|]+\|){6}\s+({target}[^\|]+)\s+\|"""
]
ParserVersion = "v1.0.0"


}
```