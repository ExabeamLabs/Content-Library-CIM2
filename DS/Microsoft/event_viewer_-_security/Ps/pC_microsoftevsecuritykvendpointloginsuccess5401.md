#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-540-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """MSWinEventLog"""
  """Successful Network Logon:"""
  """,540,"""
  """Security"""
  """Success Audit"""
  """rsa_sa_log"""
]
Fields = [
  """({event_name}Successful Network Logon)"""
  """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+),"""
  """\d{2}:\d{2}:\d{2} \d{4

}
```