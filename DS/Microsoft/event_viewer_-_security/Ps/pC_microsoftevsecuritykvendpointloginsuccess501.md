#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-501"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""AD FS Auditing"""
"""501"""
"""MSWinEventLog"""
"""Caller identity:"""
"""Security"""
]
Fields = [
"""({event_code}501)"""
"""AD FS Auditing\s+({account}[^\s]+)"""
"""({host}[^\s]+)\s+MSWinEventLog"""
"""({time}\w+ \d+ \d+:\d+:\d+ \d{1,4})\s+501"""
"""({domain}NT-[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Instance ID:\s*({instance_id}[^\s]+)"""
"""\s({email_address}[^@\s]+@[^\.]+\.[^\s]+)\s+\d+"""
"""({result}Success Audit)"""
]
ParserVersion = "v1.0.0"


}
```