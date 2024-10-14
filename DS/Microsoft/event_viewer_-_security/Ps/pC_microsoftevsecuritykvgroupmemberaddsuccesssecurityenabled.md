#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-securityenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""Security Enabled"""
"""Group Member Added"""
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""({event_name}Security Enabled [\w\s]+ Group Member Added)"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+),"""
""""agent_hostname":"({host}[^"]+)""""
""""computer":"({host}[^"]+)""""
"""(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s+)({host}[\w.\-]+)"""
"""Computer=({host}[\w\-.]+)"""
"""EventID=({event_code}\d+)"""
"""\d\d:\d\d:\d\d\s+\d\d\d\d(\s+|,)({event_code}\d+)(\s|,)+Security"""
"""Security Enabled ({group_type}[^\s]+) Group Member"""
"""Member ID:\s+(?:\%\{)?(({dest_user_sid}S-\d+-[^\s:\}]+)|(({account_domain}[^\\\s:]+)\\+)({account_name}[^\s\}:]+))\s*\}?"""
"""Target Account Name:\s+({group_name}.+?)\s+Target Domain:\s+({group_domain}[^\s]+)"""
"""Target Account ID:\s+%\{({group_id}[\w\-]+)"""
"""Caller User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:\s+\([^,\s]+[,\s]({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))\s+Member ID"""
"""Security,({event_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```