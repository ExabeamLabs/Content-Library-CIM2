#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-unlock-success-4767
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""ADAuditPlus"""
"""EVENT_NUMBER = 4767"""
"""REMARKS = A user account was unlocked."""
]
Fields = [
"""({host}[\w\-.]+)\s+ADAuditPlus"""
"""\WTIME_GENERATED\s*=\s*({time}\d{10})"""
"""\WREMARKS\s*=\s*({event_name}[^\]]+?)\s*\]"""
"""\WEVENT_NUMBER\s*=\s*({event_code}\d+)"""
"""\WEVENT_TYPE_TEXT\s*=\s*(null|({result}[^\]]+?))\s*\]"""
"""\WSOURCE\s*=\s*(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[\w\-.]+))"""
"""\WCALLER_LOGON_ID\s*=\s*(null|({login_id}[^\]]+?))\s*\]"""
"""\WCALLER_USER_DOMAIN\s*=\s*(null|({domain}[^\s\]]+?))\s*\]"""
"""\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/\"\]]+?)))\s*\]"""
"""\WCALLER_USER_NAME\s*=\s*(null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\]"""
"""\WRECORD_NUMBER\s*=\s*(null|({event_id}\d+))"""
"""\WCALLER_USER_SID\s*=\s*(null|({user_sid}[^\s\]]+))"""
"""\WFORMAT_MESSAGE\s*=\s*(null|({additional_info}.+?))\s*\]"""
"""\WACCOUNT_NAME\s*=\s*(null|({src_user}[^\s]+))"""
"""\WACCOUNT_DOMAIN\s*=\s*(null|({src_domain}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```