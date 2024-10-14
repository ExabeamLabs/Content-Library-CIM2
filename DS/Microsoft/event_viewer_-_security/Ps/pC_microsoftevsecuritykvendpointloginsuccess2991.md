#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-299-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""AD FS Auditing"""
"""299"""
"""MSWinEventLog"""
"""A token was successfully issued"""
]
Fields = [
"""({event_code}299)"""
"""AD FS Auditing\s+({account}[^\s]+)"""
"""({host}[^\s]+)\s+MSWinEventLog"""
"""({time}\w+ \d+ \d+:\d+:\d+ \d{1,4})\s+299"""
"""Instance ID:\s*({instance_id}[^\s]+)"""
"""\s({email_address}[^@\s]+@[^\.]+\.[^\s]+)\s+\d+"""
"""({result}Success Audit)"""
"""({event_name}A token was successfully issued)"""
]
ParserVersion = "v1.0.0"


}
```