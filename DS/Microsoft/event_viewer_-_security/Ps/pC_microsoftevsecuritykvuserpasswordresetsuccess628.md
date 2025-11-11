#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-reset-success-628"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""EventIDCode=628"""
]
Fields = [
"""({event_name}User Account password set)"""
"""TimeGenerated=({time}\d{10})"""
"""Computer=({dest_host}({host}[^\s]+))"""
"""EventID=({event_code}\d+)"""
"""Target Account Name:\s+({dest_user}.+?)\s+Target Domain:\s+({dest_domain}.+?)\s+Target Account ID:\s*({dest_user_sid}.+?)\s+Caller User"""
"""Caller User Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain:\s+(?=\w)({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
]
ParserVersion = "v1.0.0"


}
```