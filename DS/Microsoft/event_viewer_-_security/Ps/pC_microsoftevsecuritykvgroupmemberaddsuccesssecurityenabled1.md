#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-securityenabled-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""EvntSLog:"""
"""Group Member Added:"""
"""Security Enabled"""
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""({event_name}Security Enabled [\w\s]+ Group Member Added)"""
"""({host}[\w\-.]+)\/Security \(({event_code}\d+)\)"""
"""EvntSLog:\s+\[.+\]\s+\w+\s({time}\w+ \d+ \d+:\d+:\d+ \d+):"""
"""Security Enabled ({group_type}[^\s]+) Group Member.+?Member ID:\s+%\{(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[\w\-]+)).+?Target Account Name:\s+({group_name}.+?)\s+Target Domain:\s+({group_domain}[^\s]+).+?Target Account ID:\s+%\{({group_id}[\w\-]+).+Caller User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller Domain:\s+({domain}.+?)\s+Caller Logon ID:[^(]+\([^,]+,({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))\s+Member ID"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```