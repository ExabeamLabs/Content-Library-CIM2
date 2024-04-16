#### Parser Content
```Java
{
Name = "netskope-sc-json-file-auditlogevent"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
ExtractionType = json
Conditions = [
""""type": "admin_audit_logs""""
""""audit_log_event":"""
]
Fields = [
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.audit_log_event,exa_field_name=operation"""
  """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""
]
DupFields = [
"operation->access"
]
ParserVersion = "v1.0.0"


}
```