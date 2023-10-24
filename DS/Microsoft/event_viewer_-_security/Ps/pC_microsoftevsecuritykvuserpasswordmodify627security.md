#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-modify-627security"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""MSWinEventLog"""
""" 627 Security"""
"""Change Password Attempt:"""
]
Fields = [
"""({event_name}Change Password Attempt)"""
"""({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})"""
"""({event_code}627)"""
"""Information\s+({host}[\w.\-]+)\s+"""
"""(?:Success|Failure|Audit)\s+\w+\s+({host}[^\s]+)"""
"""Target Account Name:\s+(?=\w)({dest_user}.+?)\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
]
ParserVersion = "v1.0.0"


}
```