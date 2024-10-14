#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-securityenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""EventCode="""
"""A member was removed from a security-enabled"""
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
"""ComputerName =({host}[\w.\-]+)"""
"""EventCode=({event_code}[\w]+)"""
"""A member was removed from a security-enabled ({group_type}[^\s]+) group"""
"""Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Account Domain:\s+({domain}[^\s]+)"""
"""Logon ID:\s+({login_id}[^\s]+)\s+"""
"""Member:\s+Security ID:\s+(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\]+)\\+({account_name}.+?)|(?:.+?))\s+Account Name:"""
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