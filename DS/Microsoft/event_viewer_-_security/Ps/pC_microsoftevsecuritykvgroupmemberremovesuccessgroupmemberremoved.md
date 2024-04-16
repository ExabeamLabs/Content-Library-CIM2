#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-groupmemberremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""MSWinEventLog"""
"""Group Member Removed:"""
"""Security Enabled"""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Removed)"""
"""({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})"""
"""\d\d:\d\d:\d\d\s+\d\d\d\d\s+({event_code}\d+)\s+Security"""
"""(?:Success|Failure|Audit)\s+\w+\s+({host}[^\s]+)"""
"""Information\s+({host}[\w.\-]+)\s+"""
"""Security Enabled\s+({group_type}.+?)\s+Group Member"""
"""Member ID:\s+%\{({account_id}[\w\-]+)"""
"""Target Account Name:\s+({group_name}.+?)\s+Target Domain:\s+({group_domain}.+?)\s+Target Account ID:\s+%\{({group_id}[\w\-]+)"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\(\w+(\s|,)({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))\s+Member ID"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```