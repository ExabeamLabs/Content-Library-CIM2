#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-groupmemberremoved-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""Security Enabled"""
""" Group Member Removed"""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Removed)"""
"""EventID=({event_code}\d+)"""
"""TimeGenerated=({time}\d{10})"""
"""Computer=({dest_host}({host}[^\s]+))"""
"""Security Enabled ({group_type}[^\s]+) Group Member"""
"""Group Member.+?Member ID:\s+(%\{)?(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s]+)\\+({account_name}[^\s]+)|(?:[^\s}]+)).+Target Account Name:\s+({group_name}.+?)\s+Target Domain:\s+({group_domain}[^\s]+).+?Target Account ID:\s+%\{({group_id}[\w\-]+).+Caller User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))\s+Member ID"""
]
ParserVersion = "v1.0.0"


}
```