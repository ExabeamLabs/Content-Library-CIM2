#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-groupmemberremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Group Member Removed:"""
"""Security Enabled"""
"""EventCode="""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Removed)"""
"""ComputerName =({host}[\w.\-]+)"""
"""EventCode=({event_code}\w+)"""
"""Security Enabled ({group_type}[^\s]+) Group Member"""
"""Group Member.+?Member ID:\s+({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({dest_user_sid}.+?)|(?:.+?))\s+Target"""
"""Account Name:\s+({group_name}.+?)\s+Target"""
"""Target Domain:\s+({group_domain}[^\s]+)"""
"""Target Account ID:\s+({group_id}.+?)\s+Caller"""
"""Caller User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Caller"""
"""Caller Domain:\s+({domain}.+?)\s+Caller"""
"""Caller Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
"""Group Member.+?Member Name:\s+({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))\s+Member ID"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```