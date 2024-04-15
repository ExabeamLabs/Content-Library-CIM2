#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-modify-627"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""EventCode=627"""
"""Change Password Attempt:"""
]
Fields = [
"""({event_name}Change Password Attempt)"""
"""({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""ComputerName =({host}[\w.\-]+)"""
"""\sType=({action}.+?)\s+\w+="""
"""EventCode=({event_code}\d+)"""
"""Target Account Name:\s+(?=\w)({dest_user}.+?)\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}"""
"""Caller User Name:\s+({user}.+?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```