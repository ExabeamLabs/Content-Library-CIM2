#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-audit-policy-modify-success-612
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """EventCode=612"""
  """Audit Policy Change:"""
]
Fields = [
  """({event_name}Audit Policy Change)"""
  """ComputerName =({host}[\w.\-]+)"""
  """({event_code}612)"""
  """Changed By:.*\s+User Name:\s+({user}[\w\.\-]{1,40}\$?)"""
  """\s+Domain Name:\s+({domain}[^\s]+)"""
  """\s+Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
  """Policy Change:\s+New Policy:(({policy_name}[^\n]+)\n+)+\s*Changed By:"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```