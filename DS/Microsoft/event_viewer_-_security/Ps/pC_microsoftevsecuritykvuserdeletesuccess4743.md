#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-success-4743"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
""" [ EVENT_NUMBER = 4743 ] """
""" ADAuditPlus: """
""" [ SOURCE = """
""" [ FORMAT_MESSAGE = """
]
Fields = [
"""TIME_GENERATED\s*=\s*({time}\d{10})"""
"""({host}[\w\-.]+) ADAuditPlus"""
"""CLIENT_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[^\s\]]+))\s*\]"""
"""CLIENT_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]"""
"""CALLER_USER_NAME\s*=\s*(null|-|SYSTEM|({user}[^\s\]]+))\s*\]"""
"""CALLER_USER_DOMAIN\s*=\s*(null|-|NT AUTHORITY|({domain}[^\s\]]+))\s*\]"""
"""SOURCE\s*=\s*({src_host}[\w\-.]+)"""
"""EVENT_NUMBER\s*=\s*({event_code}\d+)"""
"""CALLER_USER_SID\s*=\s*\%?\{?({user_sid}[^\s\}]+)"""
"""CALLER_LOGON_ID\s*=\s*(null|-|({login_id}[^\s]+))"""
"""ACCOUNT_NAME\s*=\s*(null|-|({object}[^\s]+))"""
"""REMARKS\s*=\s*(null|-|({event_name}[^.\]]+))(\.)?\s+\]"""
"""FORMAT_MESSAGE\s*=\s*(null|-|({additional_info}[^.\]]+))(\.)?\s+\]"""
"""Category\s*=\s*({category}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```