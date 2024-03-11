#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-log-clear-success-auditlogclear
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """\t517\t""", """The audit log was cleared""" ]
  Fields = [
    """({event_name}The audit log was cleared)""",
    """\s+(Information|Audit Success|Success Audit)\s+({host}[\w.\-]+)""",
    """\s+(Information|Audit Success|Success Audit)\s+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))"""
    """\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+""",
    """({event_code}517)""",
    """({event_name}The audit log was cleared)""",
    """\s+Client User Name:\s+({user}.+?)\s+Client Domain""",
    """\s+Client Domain:\s+({domain}[^\s]+)""",
    """\s+Client Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```