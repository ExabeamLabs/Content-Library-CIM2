#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-680-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """(680)"""
  """Logon attempt by:"""
]
Fields = [
  """({event_name}Logon attempt)"""
  """({time}\w+ \d{1,2} [\d:]+ \d+):"""
  """\d{4}:[\s/]([^/]+)\/Security"""
  """/Security \(({event_code}680)\)"""
  """Logon account:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation:\s+({dest_host}[\w\-.]+)"""
  """Error Code:\s+({result_code}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```