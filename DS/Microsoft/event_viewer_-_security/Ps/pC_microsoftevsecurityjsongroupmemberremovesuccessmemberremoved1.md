#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-memberremoved-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""Security ID:"""
"""Logon ID:"""
"""A member was removed from a security-enabled"""
]
Fields = [
""""created\\*":\\*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""({event_code}\d+)\|\s+devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
""""_raw":"({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
""""agent_hostname":"({host}[^"]+)""""
""""computer":"({host}[^"]+)""""
"""(?i)(success|audit)\s+\w+\s+({host}[\w\-.]+)\s"""
""""?Event(ID>)?(Code["\s]*(:|=|\\=)\s*"?)?({event_code}\d+)"""
"""({event_code}\d+)\s+Microsoft-Windows-Security-Auditing"""
"""A member was removed from a security-enabled\s*({group_type}[^\s]+)\s+group"""
"""Account Name\s*:((\\)*[rnt])*\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*((\\)*[rnt])*Account Domain\s*:((\\)*[rnt])*\s*({domain}[^\s\\:]+)"""
"""Logon ID:\s*({login_id}[^\s]+)\s+"""
"""Member:\s*Security ID\s*:\s*(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\\s]+)\\+({account_name}[^\\\s]+)|(?:.*?))\s*Account Name:"""
"""Account Name\s*:\s*(.+?({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))|(?:.+?))\s*Group:"""
"""Group\s*:\s*Security ID\s*:\s*({group_id}[^\s]+)\s*"""
"""Group:.+?(Group|Account) Name\s*:(\\*(r|n|t|\s))*({group_name}.+?)?(\\*(r|n|t|\s))*(Group|Account) Domain\s*:(\\*(r|n|t))*\s*({group_domain}.+?)?(\\*(r|n|t|\s))*Additional Information:"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```