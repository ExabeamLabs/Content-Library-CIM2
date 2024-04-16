#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-lock-success-4800-3
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=4800"""
  """The workstation was locked"""
]
Fields = [
  """EventID=({event_code}\d+)"""
  """({event_name}The workstation was locked)"""
  """TimeGenerated=({time}\d{10})"""
  """Computer=({host}[^\s]+)"""
  """Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain"""
  """Account Domain:\s+({domain}.+?)\s+Logon ID"""
  """Logon ID:\s+({login_id}[^\s]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```