#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-member-remove-success-memberremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Security ID:"""
"""Logon ID:"""
"""A member was removed from a security-enabled"""
"""Computer"""
"""<EventID>4733</EventID>"""
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""Computer(Name|_name)?(["\s]*(:|=|\\=)\s*")?>?({host}[\w\-.]+)(<|"|\s)"""
""""?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)"""
"""({event_code}\d+)\s+Microsoft-Windows-Security-Auditing"""
"""A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group"""
"""Account Name\s*:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain\s*:\s*({domain}[^\s]+)\s+""",
"""Logon ID:\s*({login_id}[^\s]+)\s+"""
"""Member:\s*Security ID\s*:\s*(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s]+)\\+({account_name}[^\\\s]+)|(?:.*?))\s*Account Name:"""
"""Account Name\s*:\s*(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:"""
"""Group\s*:\s*Security ID\s*:\s*({group_id}[^\s]+)\s*"""
"""Group:\s*[^$]+?(Group|Account) Name\s*:\s*({group_name}.+?)?\s*(Group|Account) Domain\s*:\s*({group_domain}[^\s]+)\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```