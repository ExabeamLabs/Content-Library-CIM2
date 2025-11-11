#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-delete-success-4730
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = ["""EVENT_NUMBER = 4730""","""A security-enabled global group was deleted"""]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})""",
    """({dest_host}({host}[\w\-.]+)) ADAuditPlus""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """CALLER_LOGON_ID\s*=\s*({login_id}[^]]+?)\s*\]""",
    """ACCOUNT_DOMAIN\s*=\s*({domain}[^]]+?)\s*\]""",
    """\sPROCESS_ID\s*=\s*(null|({process_id}[^]]+?))\s*\]""",
    """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]"""
    """CALLER_USER_NAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\]""",
    """CALLER_USER_SID\s*=\s*(({user_sid}[^]]+?))\s*\]""",
  ]


}
```