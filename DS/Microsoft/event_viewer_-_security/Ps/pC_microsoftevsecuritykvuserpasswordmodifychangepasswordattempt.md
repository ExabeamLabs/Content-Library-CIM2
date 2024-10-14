#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-modify-changepasswordattempt"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""Change Password Attempt:"""
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""({event_name}Change Password Attempt)"""
"""({time}\w+ \d{1,2} [\d:]+ \d+)"""
"""Security,({event_id}\d+)"""
"""\sType=({result}.+?)\s+\w+="""
"""(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s)({host}[\w\-.]+)"""
"""({host}[\w\-.]+)\/Security"""
"""Computer=({host}[\w\-.]+)"""
"""\s+({result}(?i)((audit|success|failure)( |_)(success|audit|failure)))\s+"""
"""({event_code}627)"""
"""Target Account Name\s*:\s*(?=\w)({dest_user}.+?)\s+Target Domain\s*:\s*(?=\w)({dest_domain}.+?)\s+Target Account ID\s*:\s*(\%\{)?({dest_user_sid}[^}:]+?)(?:\s+|\})"""
"""Caller User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
"""Caller User Name\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain\s*:\s*({domain}.+?)\s+Caller Logon ID\s*:\s*\([^,\s]+[,\s]({login_id}[^\)]+)"""
]
ParserVersion = "v1.0.0"


}
```