#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-5136-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""5136"""
"""A directory service object was modified"""
"""Directory Service:"""
"""Application Correlation ID:"""
]
Fields = [
"""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""({event_name}A directory service object was modified)"""
""""agent_hostname":"({dest_host}({host}[\w\-.]+))""""
""""computer":"({dest_host}({host}[\w\-.]+))""""
"""(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({dest_host}({host}[\w.-]+))\s"""
"""__li_source_path="*({dest_host}({host}[\w\-.]+))""""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""Computer(Name)?\s*\\*"?(=|:|>)\s*"*({dest_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)"""
"""Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({dest_host}({host}[\w.\-]+)))"""
"""\WTimeGenerated=({time}\d+)"""
"""({event_code}5136)"""
"""\sSubject:[^\}\]]+?\sAccount Name:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
"""\sSubject:[^\}\]]+?\sAccount Domain:\s*({domain}[^\s]+)"""
"""\sSubject:[^\}\]]+?\sLogon ID:\s*({login_id}[^\s]+)"""
"""Object:.+?Class:\s+({object_type}.+?)\s+Attribute:"""
"""Attribute:[^\}\]]+?LDAP Display Name:\s*({attribute}.+?)\s+Syntax"""
"""Object:\s*DN:\s*({ds_object_dn}.+?)\s+GUID:"""
"""\sClass:\s*({class_name}[^:]+?)\s*\w+:"""
""""hostname":"({dest_host}({host}[\w\-.]+))""""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
""""EventID\\?":({event_code}\d+)"""
""""ProviderGuid\\?":\\?"({process_guid}[^"\\]+)\\?""""
"""Directory Service:\s*Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)"""
"""\sType:\s*({additional_info}[^:]+?)\s*\w+:"""
"""\sValue:\s*({attribute_value}[^:]+?)\s*\w+:"""
]
ParserVersion = "v1.0.0"


}
```