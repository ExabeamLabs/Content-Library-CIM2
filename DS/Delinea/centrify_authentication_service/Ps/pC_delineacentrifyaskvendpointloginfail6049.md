#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-fail-6049"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """SourceName =Centrify AuditTrail"""
  """AUDIT_TRAIL|Centrify Suite|DirectAuthorize - Windows|"""
  """|PowerShell remote connection failure|"""
  """EventCode=6049"""
]
Fields = [
  """:\d\d\s\w+\s*({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
  """ComputerName =({dest_host}[^\.]+)\.({domain}[^\s]+)"""
  """User=(NULL|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
  """Sid=({user_sid}[^\s]+?)\sSidType"""
  """EventCode=({event_code}6049)"""
  """AUDIT_TRAIL\|Centrify Suite\|DirectAuthorize - Windows[^=]+?({event_name}PowerShell remote connection failure)"""
  """reason=({failure_reason}[^=]+)\.(\s+\w+=)?"""
  """Message:\s*({additional_info}[^:]+)\.\s+"""
]
ParserVersion = "v1.0.0"


}
```