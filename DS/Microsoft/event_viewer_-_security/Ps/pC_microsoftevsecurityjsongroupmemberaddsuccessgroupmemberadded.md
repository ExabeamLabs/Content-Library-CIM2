#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-groupmemberadded"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""LogName ="""
"""SourceName ="""
"""Group Member Added:"""
"""Security Enabled"""
"""EventCode="""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Added)"""
"""ComputerName =({dest_host}({host}[\w.\-]+))"""
"""EventCode=({event_code}\w+)"""
"""Security Enabled ({group_type}[^\s]+) Group Member"""
"""Group Member.+?Member ID:\s+(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s:]+)\\+({account_name}.+?)|(?:.+?))\s+Target Account"""
"""Target Account Name:\s+({group_name}.+?)\s+Target"""
"""Target Domain:\s+({group_domain}[^\s]+)"""
"""Target Account ID:\s+({group_id}.+?)\s+Caller"""
"""Caller User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Caller"""
"""Caller Domain:\s+({domain}.+?)\s+Caller"""
"""Caller Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))\s+Member ID"""
]
ParserVersion = "v1.0.0"


}
```