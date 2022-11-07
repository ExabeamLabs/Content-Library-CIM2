#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-audit-policy-modify-success-4719-2
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventCode=4719"""
  """System audit policy was changed"""
]
Fields = [
  """({event_name}System audit policy was changed)"""
  """ComputerName =({host}[\w.\-]+)"""
  """({time}\d\d/\d\d/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))\s+"""
  """EventCode=({event_code}\d+)"""
  """\s+Account Name:\s+({user}.+?)\s+Account Domain"""
  """\s+Account Domain:\s+({domain}[^\s]+)"""
  """\s+Logon ID:\s+({login_id}[^\s]+)"""
  """\s+Category:\s+({audit_category}.+?)\s+Subcategory:"""
  """\s+Subcategory:\s+({sub_category}.+?)\s+Subcategory GUID:"""
  """\s+Changes:\s+({policy_name}[^:]+?)(\s+\d+|\s*$)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```