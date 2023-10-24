#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-47"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyyMMddHHmmss.SSS"
Conditions = [
"""EventCode = 47"""
"""A member was removed from a security-enabled """
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
"""Computer(Name)? = "+({host}[^"]+)""""
"""EventCode = ({event_code}\d+)"""
"""TimeGenerated = "({time}[\d]+.\d\d\d)"""
"""A member was removed from a security-enabled ({group_type}[^\s]+) group"""
"""Subject:.+?Account Name:\s+({user}[\w\.\-]{1,40}\$?)"""
"""Account Domain:\s+({domain}[^\s]+)"""
"""Logon ID:\s+({login_id}[^\s]+)\s+"""
"""Member:\s+Security ID:\s+({account_id}(?=[^\\]+\\)({sid_domain}[^\\]+)\\({dest_user_sid}.+?)|(?:.+?))\s+Account Name:"""
"""Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s+Group:"""
"""Group:\s+Security ID:\s+({group_id}[^\s]+)"""
"""Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:"""
"""Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```