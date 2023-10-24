#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-success-54206"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""SourceName =Centrify AuditTrail"""
"""AUDIT_TRAIL|Centrify Suite|MFA|"""
"""|MFA challenge succeeded|"""
"""EventCode=54206"""
]
Fields = [
""":\d\d\s\w+\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
"""entityname=({domain}[^\\]+)\\({dest_host}[^\s]+)"""
"""User=(NULL|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
"""Sid=({user_sid}[^\s]+?)\sSidType"""
"""EventCode=({event_code}54206)"""
"""AUDIT_TRAIL\|Centrify Suite\|MFA\|[^=]+({event_name}MFA challenge succeeded)"""
"""Message:\s*({additional_info}[^:]+)\.\s+"""
]
ParserVersion = "v1.0.0"


}
```