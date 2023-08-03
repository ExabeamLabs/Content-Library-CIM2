#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-create-success-624
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""User Account Created"""
"""Caller Logon ID:"""
"""Attributes:"""
"""New Account Name:"""
]
Fields = [
"""({event_name}User Account Created)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""({event_code}624)"""
"""({host}[^\/\s]+)\/Security \(624\)"""
"""Computer=({host}[^\s]+)"""
"""New Account Name:\s+({account_name}.+?)\s+New Domain:\s+({account_domain}[^\s]+)\s+New Account ID:\s+(%\{)?({account_id}[^\s\}]+)"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}[^\s]+)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
]
DupFields = [
"host->dest_host",
"account_name->dest_user"
]
ParserVersion = "v1.0.0"


}
```