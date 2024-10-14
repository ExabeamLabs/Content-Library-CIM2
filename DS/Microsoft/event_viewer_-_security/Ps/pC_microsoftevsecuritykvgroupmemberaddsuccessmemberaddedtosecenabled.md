#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-memberaddedtosecenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""A member was added to a security-enabled"""
]
Fields = [
"""({event_name}A member was added to a security-enabled [\w\s]+ group)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""shost=({host}[^\s]+)"""
"""A member was added to a security-enabled ({group_type}\w+) group"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""duser=({user_dn}.+?)\s+\w+="""
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