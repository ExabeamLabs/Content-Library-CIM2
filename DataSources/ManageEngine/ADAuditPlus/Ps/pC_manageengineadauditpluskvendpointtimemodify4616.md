#### Parser Content
```Java
{
Name = manageengine-adauditplus-kv-endpoint-time-modify-4616
  ParserVersion = v1.0.0
  Vendor = ManageEngine
  Product = ADAuditPlus
  TimeFormat = "epoch_sec"
  Conditions = ["""EVENT_NUMBER = 4616""","""The system time was changed"""]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d+)""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """({event_name}The system time was changed)""",
    """\sACCOUNT_NAME\s*=\s*(({user}[^]]+?))\s*\]""",
    """\sACCOUNT_DOMAIN\s*=\s*({domain}[^]]+?)\s*\]""",
    """\sPROCESS_ID\s*=\s*({process_id}[^]]+?)\s*\]""",
    """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]""",
    """CALLER_USER_SID\s*=\s*(({user_sid}[^]]+?))\s*\]"""
  ]
  DupFields = [ "host->dest_host" ]


}
```