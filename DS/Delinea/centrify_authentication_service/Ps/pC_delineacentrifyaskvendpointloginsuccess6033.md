#### Parser Content
```Java
{
Name = "delinea-centrifyas-kv-endpoint-login-success-6033"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """SourceName =Centrify AuditTrail"""
  """AUDIT_TRAIL|Centrify Suite|DirectAuthorize - Windows|"""
  """|Remote login success|"""
  """EventCode=6033"""
]
Fields = [
  """:\d\d\s\w+\s*({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
  """entityname=({domain}[^\\]+)\\({dest_host}[^\s]+)"""
  """User=(NULL|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
  """Sid=({user_sid}[^\s]+?)\sSidType"""
  """EventCode=({event_code}6033)"""
  """AUDIT_TRAIL\|Centrify Suite\|DirectAuthorize - Windows[^=]+?({event_name}Remote login success)"""
  """Message:\s*({additional_info}[^:]+)\.\s+"""
]
ParserVersion = "v1.0.0"


}
```