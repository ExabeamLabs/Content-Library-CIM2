#### Parser Content
```Java
{
Name = manageengine-adauditplus-kv-scheduled-task-delete-4699
  ParserVersion = v1.0.0
  Vendor = ManageEngine
  Product = ADAuditPlus
  TimeFormat = "epoch_sec"
  Conditions = ["""EVENT_NUMBER = 4699""","""A scheduled task was deleted"""]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """({event_name}A scheduled task was deleted)""",
    """CALLER_LOGON_ID\s*=\s*(null|({login_id}[^]]+?))\s*\]""",
    """ACCOUNT_DOMAIN\s*=\s*({domain}[^]]+?)\s*\]""",
    """\sPROCESS_ID\s*=\s*(null|({process_id}[^]]+?))\s*\]""",
    """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]"""
    """ACCOUNT_NAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\]""",
    """CALLER_USER_SID\s*=\s*(({user_sid}[^]]+?))\s*\]""",
    """FILE_NAME\s*=\s*({task_name}[^\s\]]+)\s*\]""",
    """REPORT_PROFILE\s*=\s*[^\]]+?for ({src_host}[^\]]+?)\s*\]"""
  ]
  DupFields = [ "host->dest_host" ]


}
```