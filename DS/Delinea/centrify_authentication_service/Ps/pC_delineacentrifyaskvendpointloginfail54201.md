#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-fail-54201"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""SourceName =Centrify AuditTrail"""
"""AUDIT_TRAIL|Centrify Suite|MFA|"""
"""|MFA challenge failed|"""
"""EventCode=54201"""
]
Fields = [
""":\d\d\s\w+\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
"""ComputerName =({dest_host}[^\.]+)\.({domain}[^\s]+)"""
"""User=(NULL|NOT_TRANSLATED|({user}[^\s]+))"""
"""Sid=({user_sid}[^\s]+?)\sSidType"""
"""EventCode=({event_code}54201)"""
"""AUDIT_TRAIL\|Centrify Suite\|MFA\|[^=]+({event_name}MFA challenge failed)"""
"""reason=({failure_reason}[^=]+)\."""
"""Message:\s*({additional_info}[^:]+)\s+\.\s+"""
]
ParserVersion = "v1.0.0"


}
```