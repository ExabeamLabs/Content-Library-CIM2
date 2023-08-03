#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-unlock-success-4801-4
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventCode=4801"""
  """The workstation was unlocked."""
]
Fields = [
  """({event_name}The workstation was unlocked)"""
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))\s+LogName ="""
  """({event_code}4801)"""
  """ComputerName =({host}[^\s]+)"""
  """Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:"""
  """Account Domain:\s+({domain}.+?)\s+Logon ID:"""
  """Logon ID:\s+({login_id}[^\s]+)\s+Session"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```