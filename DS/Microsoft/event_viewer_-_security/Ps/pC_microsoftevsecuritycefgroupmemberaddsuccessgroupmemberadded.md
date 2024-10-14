#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-add-success-groupmemberadded"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Security:6"""
"""Security Enabled"""
"""Group Member Added"""
]
Fields = [
"""({event_name}Security Enabled [\w\s]+ Group Member Added)"""
"""Security:({event_code}\d+)"""
"""\|Security Enabled ({group_type}\w+)"""
"""\srt=({time}\d{13})"""
"""\ssntdom=({domain}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\ssuid=\([^,]+,({login_id}[^\)]+)"""
"""\sdntdom=({group_domain}[^\s]+)"""
"""duser=({group_name}.+?)\s+\w+="""
"""\scs6=({user_dn}.+?)\s+\w+="""
"""\scs6=(.+?CN\\?=.+?,({user_ou}(OU)?.+?DC\\?=[\w-]+))\s\w+="""
"""\sdvchost=({host}[^\s]+)"""
"""\sduid=({group_id}.+?)\s+\w+="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```