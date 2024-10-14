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
  """ComputerName =(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))"""
  """Client User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """({event_code}517)"""
  """\s+Client Domain:\s+({domain}[^\s]+)"""
  """\s+Client Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
]
ParserVersion = "v1.0.0"


}
```