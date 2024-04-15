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
  """\d{2}:\d{2}:\d{2} \d{4},({event_code}[^,]+),Security"""
  """Security,({event_id}\d+)"""
  """User Name:\s+({user}.+?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+\([^,\s]+[,\s]({login_id}[^\)]+)\)\s+Logon Type:\s+({login_type}\d+)\s+Logon Process:\s+({process_path}.+?)\s+Authentication Package"""
  """Logon Process:\s+({auth_process}.+?)\s+Authentication Package:\s+({auth_package}[^\s]+)"""
  """Workstation Name:\s+({src_host_windows}[^\s]+)\s+Logon"""
  """Workstation Name:\s+({src_host}[^\s]+)\s+Logon.*?Source Network Address:\s*-\s+"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```