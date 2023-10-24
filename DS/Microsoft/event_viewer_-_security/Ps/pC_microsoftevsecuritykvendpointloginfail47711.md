#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4771-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """Kerberos pre-authentication failed"""
  """,4771,Microsoft-Windows-Security-Auditing"""
  """rsa_sa_log"""
]
Fields = [
  """({event_name}Kerberos pre-authentication failed)"""
  """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
  """Security,(rn=)?({event_id}[\d]+)"""
  """Failure Audit,({host}[^,]+)"""
  """\d{2}:\d{2}:\d{2} \d{4

}
```