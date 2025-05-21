#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-audit-policy-modify-success-4719-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""     4719    """
"""System audit policy was changed"""
"""Audit Policy Change"""
]
Fields = [
"""({event_name}System audit policy was changed)"""
"""\s+(Information|Audit Success|Success Audit)\s+({host}[\w.\-]+)"""
"""({host}[^\s=]+)\sMSWinEventLog"""
"""\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+"""
"""({event_code}4719)"""
"""\s+Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain"""
"""\s+Account Domain:\s+({domain}[^\s]+)"""
"""\s+Logon ID:\s+({login_id}[^\s]+)"""
"""\s+Category:\s+({audit_category}.+?)\s+Subcategory:"""
"""\s+Subcategory:\s+({sub_category}.+?)\s+Subcategory GUID:"""
"""\s+Changes:\s+({audit_policy_name}.+?)\s+\d+"""
]
ParserVersion = "v1.0.0"


}
```