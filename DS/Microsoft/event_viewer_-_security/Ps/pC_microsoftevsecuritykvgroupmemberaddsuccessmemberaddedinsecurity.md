#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-memberaddedinsecurity"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""LogName ="""
"""SourceName ="""
"""EventCode="""
"""A member was added to a security-enabled"""
]
Fields = [
"""({event_name}A member was added to a security-enabled [\w\s]+ group)"""
"""ComputerName =({host}[\w.\-]+)"""
"""EventCode=({event_code}[\w]+)"""
"""A member was added to a security-enabled ({group_type}[^\s]+) group"""
"""Subject:.+?Account Name:\s+({user}[\w\.\-]{1,40}\$?)"""
"""Account Domain:\s+(\\t)?({domain}[^\s]+)"""
"""Logon ID:\s+(\\t)?({login_id}[^\s]+)\s+"""
"""Member:\s+Security ID:\s+({dest_user_sid}[^:]+?)\s+Account Name:"""
"""Member:(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s+Group:"""
"""Group:\s+(\\r\s\\t)?Security ID:\s*(\\t)?({group_id}[^\s]+)(.+?)(\\r\s\\t)?Group Name:"""
"""Group:.+?(Group|Account) Name:\s+(\\t)?({group_name}.+?)?\s*(\\r\s\\t)?(Group|Account) Domain:"""
"""Group:.+?(Group|Account) Domain:\s+(\\t)?({group_domain}[^\s]+)"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```