#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""MSWinEventLog"""
"""5136"""
"""A directory service object was modified"""
]
Fields = [
"""({event_name}A directory service object was modified)"""
"""({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})"""
""""event_time":"({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d)"""
"""(Information|Success Audit|Audit Success)\s+({host}[^\s]+)"""
""""ComputerName":"({host}[\w\-.]+)"""
"""({event_code}5136)"""
"""Subject:.+?Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}[^\s]+)"""
"""Object:.+?Class:\s*({ds_object_class}.+?)\s*Attribute:"""
"""Attribute:.+?LDAP Display Name:\s*({attribute}.+?)\s*Syntax"""
"""Object:\s*DN:\s*({ds_object_dn}.+?)\s*GUID:"""
"""Object:\s*DN:.+?({ds_object_ou}OU.+?)\s*GUID:"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```