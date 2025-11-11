#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-memberwasremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Security ID:"""
"""Logon ID:"""
"""A member was removed from a security-enabled"""
"""_raw"""
"""Computer"""
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
""""_raw":"({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
"""Computer(Name|_name)?(["\s]*(:|=|\\=)\s*")?>?({dest_host}({host}[\w\-.]+))(<|"|\s)"""
""""?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)"""
"""({event_code}\d+)\s+Microsoft-Windows-Security-Auditing"""
"""A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group"""
"""Account Name\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain\s*:\s*({domain}[^\s]+)\s+"""
"""Logon ID:\s*({login_id}[^\s]+)\s+"""
"""Member:\s*Security ID\s*:\s*(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s]+)\\+({account_name}[^\\\s]+)|(?:.*?))\s*Account Name:"""
"""Account Name\s*:\s*(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:"""
"""Group\s*:\s*Security ID\s*:\s*({group_id}[^\s]+)\s*"""
"""Group:.+?(Group|Account) Name\s*:\s*({group_name}.+?)?\s*(Group|Account) Domain\s*:\s*({group_domain}[^\s]+)\s*"""
]
ParserVersion = "v1.0.0"


}
```