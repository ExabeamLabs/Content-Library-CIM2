#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-remove-success-securityenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""A member was removed from a security-enabled"""
]
Fields = [
"""({event_name}A member was removed from a security-enabled [\w\s]+ group)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""shost=({host}[^\s]+)"""
"""A member was removed from a security-enabled ({group_type}\w+) group"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}.+?)\s+\w+="""
"""duser=({user_sid}[^\s]+)\s+\w+="""
"""nitroObjectID=({group_name}.+?)\s+\w+="""
"""nitroSecurity_ID=({account_id}[^\s]+)"""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```