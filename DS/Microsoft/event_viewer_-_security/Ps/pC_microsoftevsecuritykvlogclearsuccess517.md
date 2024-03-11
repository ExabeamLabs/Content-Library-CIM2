#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-log-clear-success-517
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """EventCode=517"""
  """The audit log was cleared"""
]
Fields = [
  """({event_name}The audit log was cleared)"""
  """ComputerName =({host}[\w.\-]+)"""
  """ComputerName =(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))"""
  """Client User Name:\s+({user}[^\s]+)"""
  """({event_code}517)"""
  """\s+Client Domain:\s+({domain}[^\s]+)"""
  """\s+Client Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
]
ParserVersion = "v1.0.0"


}
```