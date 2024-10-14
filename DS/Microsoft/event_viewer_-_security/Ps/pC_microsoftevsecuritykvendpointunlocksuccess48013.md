#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-unlock-success-4801-3
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=4801"""
  """The workstation was unlocked"""
]
Fields = [
  """EventID=({event_code}\d+)"""
  """({event_name}The workstation was unlocked)"""
  """TimeGenerated=({time}\d{10})"""
  """Computer=({host}[\w\-.]+)"""
  """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain"""
  """Account Domain:\s+({domain}.+?)\s+Logon ID"""
  """Logon ID:\s+({login_id}[^\s]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```