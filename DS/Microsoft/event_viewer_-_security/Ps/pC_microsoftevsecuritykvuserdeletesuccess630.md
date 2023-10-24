#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-delete-success-630
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""User Account Deleted"""
"""Caller User Name:"""
"""Logon ID:"""
"""Target Account Name:"""
]
Fields = [
"""({event_name}User Account Deleted)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""Security,({event_id}[\d]+),(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
"""({event_code}630)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[\w.\-]+)"""
"""({host}[^\/\s]+)\/Security \(630\)"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[\w\-.]+?)(\"|\s)"""
"""Target Account Name:\s+(?=\w)({dest_user}.+?)\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
]
DupFields = [
"host->dest_host"
"dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```