#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-reset-success-accountpasswordset"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""User Account password set:"""
]
Fields = [
"""({event_name}User Account password set)"""
"""({time}\w+ \d{1,2} [\d:]+ \d+)"""
"""(?i)(information)(,|\s+)({host}[\w.\-]+)"""
"""(?i)((audit|success|failure)( |_)(success|audit|failure))\s+({host}[\w\-.]+)\s+Account Management"""
"""({host}[^\/\s]+)\/Security"""
"""ComputerName =({host}[\w.\-]+)"""
"""({event_code}628)"""
"""Target Account Name:\s+({dest_user}.+?)\s+Target Domain:\s+({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}"""
"""Caller User Name:\s+(?=\w)?({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+(?=\w)({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\(.+?\s+({login_id}[^\s)]+)\)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```