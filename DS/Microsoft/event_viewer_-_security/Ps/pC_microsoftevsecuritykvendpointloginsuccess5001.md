#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-500-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""AD FS Auditing"""
"""500"""
"""MSWinEventLog"""
"""Issued identity:"""
]
Fields = [
"""({event_code}500)"""
"""AD FS Auditing\s+({account}[^\s]+)"""
"""({host}[^\s]+)\s+MSWinEventLog"""
"""({time}\w+ \d+ \d+:\d+:\d+ \d{1,4})\s+500"""
"""({domain}NT-[^\\]+)\\({user}[^\s<]+)"""
"""Instance ID:\s*({iid}[^\s]+)"""
"""\s({email_address}[^@\s]+@[^\.]+\.[^\s]+)\s+\d+"""
"""({action}Success Audit)"""
]
ParserVersion = "v1.0.0"


}
```