#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-audit-policy-modify-success-4719-2
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=4719"""
  """System audit policy was changed"""
]
Fields = [
  """({event_name}System audit policy was changed)"""
  """TimeGenerated=({time}\d{10})"""
  """EventIDCode=({event_code}\d+)"""
  """\s+Account Name:\s+(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain"""
  """\s+Account Domain:\s+({domain}[^\s]+)"""
  """\s+Logon ID:\s+({login_id}[^\s]+)"""
  """\s+Category:\s+({audit_category}.+?)\s+Subcategory:"""
  """\s+Subcategory:\s+({sub_category}.+?)\s+Subcategory GUID:"""
  """\s+Changes:\s+({policy_name}.+?)\s*(\w+:|$)"""
  """\s+Computer=({src_host}({host}[\w.\-]+))"""
]
ParserVersion = "v1.0.0"


}
```