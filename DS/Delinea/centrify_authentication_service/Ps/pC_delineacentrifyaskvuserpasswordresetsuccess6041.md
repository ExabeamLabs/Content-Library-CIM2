#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-user-password-reset-success-6041"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""SourceName =Centrify AuditTrail"""
"""AUDIT_TRAIL|Centrify Suite|DirectAuthorize - Windows|"""
"""|Self-service password reset failure|"""
"""EventCode=6041"""
]
Fields = [
""":\d\d\s\w+\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
"""ComputerName =({dest_host}[^\.]+)\.({domain}[^\s]+)"""
"""User=(NULL|NOT_TRANSLATED|({user}[^\s]+))"""
"""Sid=({user_sid}[^\s]+?)\sSidType"""
"""EventCode=({event_code}6041)"""
"""AUDIT_TRAIL\|Centrify Suite\|DirectAuthorize - Windows[^=]+({event_name}Self-service password reset failure)"""
"""reason=({failure_reason}[^=]+)\.?""""
"""Message:\s*({additional_info}[^:]+)\.\s+"""
]
ParserVersion = "v1.0.0"


}
```