#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-group-member-remove-success-memberremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""Group Member Removed:"""
"""Security Enabled"""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Removed)"""
"""TimeGenerated=({time}\d{10})"""
"""(?i)(success|failure|audit)\s+\w+\s+({host}[\w\-.]+)"""
"""Information(,|\s+)({host}[\w.\-]+)"""
"""Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s)"""
"""Event(Code|ID)=({event_code}\d+)"""
"""\d\d:\d\d:\d\d\s+\d\d\d\d\s+({event_code}\d+)\s+Security"""
"""Security Enabled\s+({group_type}[^\s]+)\s+Group Member"""
"""Group Member.+?Member ID:\s+(%\{)?({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({dest_user_sid}[^\s]+)|(?:[^\s}]+)).+Target"""
"""Target Account Name:\s+({group_name}.+?)\s+Target Domain:\s+({group_domain}[^\s]+).+?Target Account ID:\s+%\{({group_id}[\w\-]+).+Caller"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,\s]+(\s|,)({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))\s+Member ID"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```