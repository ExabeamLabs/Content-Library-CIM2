#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-audit_policy-modify-success-auditpolicychange
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "\t612\t", "Audit Policy Change:" ]
  Fields = [
    """({event_name}Audit Policy Change)""",
    """\s+(Information|Audit Success|Success Audit)\s+({host}[\w.\-]+)""",
    """\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+""",
    """({event_code}612)""",
    """\s+User Name:\s+({user}.+?)\s+Domain""",
    """\s+Domain Name:\s+({domain}[^\s]+)""",
    """\s+Logon ID:\s+\([^,]+,({login_id}[^)]+)""",
    """\s+New Policy:\s+({policy_name}.+?)\s+Changed By"""
  ]
  DupFields = [ "host->src_host" ]
  ParserVersion = "v1.0.0"


}
```