#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-lock-success-4800-4
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """ EventCode=4800"""
  """The workstation was locked."""
]
Fields = [
  """({event_name}The workstation was locked)"""
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))\s+LogName ="""
  """({event_code}4800)"""
  """ComputerName =({host}[^\s]+)"""
  """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
  """Account Domain:\s+({domain}.+?)\s+Logon ID:"""
  """Logon ID:\s+({login_id}[^\s]+)\s+Session"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```