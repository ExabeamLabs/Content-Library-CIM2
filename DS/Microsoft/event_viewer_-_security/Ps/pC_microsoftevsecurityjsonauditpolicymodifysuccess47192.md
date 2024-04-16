#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-audit-policy-modify-success-4719-2
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=4719"""
  """System audit policy was changed"""
]
Fields = [
  """({event_name}System audit policy was changed)"""
  """ComputerName =({host}[\w.\-]+)"""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  """EventCode=({event_code}\d+)"""
  """\sAccount Name:\s*({user}[\w\.\-]{1,40}\$?)\s+Account Domain"""
  """\sAccount Domain:\s*({domain}[^\s]+)"""
  """\sLogon ID:\s*({login_id}[^\s]+)"""
  """\sCategory:\s*({audit_category}[^:]+?)\s+Subcategory:"""
  """\sSubcategory:\s*({sub_category}[^:]+?)\s+Subcategory GUID:"""
  """\sChanges:\s*({policy_name}[^:]+?)(\s+\d+|\s*$|\s*")"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```