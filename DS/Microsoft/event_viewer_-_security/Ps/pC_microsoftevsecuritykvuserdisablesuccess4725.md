#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""ADAuditPlus"""
"""EVENT_NUMBER = 4725"""
"""A user account was disabled"""
]
Fields = [
"""TIME_GENERATED\s*=\s*({time}\d{10})"""
"""({host}[\w\-.]+) ADAuditPlus"""
"""CALLER_USER_NAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""CALLER_USER_DOMAIN\s*=\s*({domain}[^\s\]]+)"""
"""SOURCE\s*=\s*({src_host}[\w\-.]+)"""
"""RECORD_NUMBER\s*=\s*({event_id}\d+)"""
"""EVENT_NUMBER\s*=\s*({event_code}\d+)"""
"""CALLER_USER_SID\s*=\s*({user_sid}[^\s]+)"""
"""CALLER_LOGON_ID\s*=\s*({login_id}[^\s]+)"""
"""ACCOUNT_NAME\s*=\s*({dest_user}[^\s]+)"""
"""ACCOUNT_DOMAIN\s*=\s*({dest_domain}[^\s]+)"""
"""ACCOUNT_SID\s*=\s*\%\{({dest_user_sid}[^\s\}]+)"""
]
ParserVersion = "v1.0.0"


}
```