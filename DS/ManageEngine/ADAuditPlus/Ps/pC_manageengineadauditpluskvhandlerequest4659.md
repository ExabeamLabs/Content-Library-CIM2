#### Parser Content
```Java
{
Name = manageengine-adauditplus-kv-handle-request-4659
  ParserVersion = v1.0.0
  Vendor = ManageEngine
  Product = ADAuditPlus
  TimeFormat = "epoch_sec"
  Conditions = ["""EVENT_NUMBER = 4659""","""An object was deleted"""]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d+)""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """({event_name}An object was deleted)""",
    """\sOBJECT_NAME\s*=\s*({object}[^]]+?)\s*\]""",
    """\sLOGON_ID\s*=\s*({login_id}[^]]+?)\s*\]""",
    """\sDOMAIN\s*=\s*({domain}[^]]+?)\s*\]""",
    """\sACCESSES\s*=\s*({access}[^]]+?)\s*\]""",
    """\sPROCESS_ID\s*=\s*({process_id}[^]]+?)\s*\]""",
    """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]"""
    """\sUSERNAME\s*=\s*(({user}[^]]+?))\s*\]""",
    """\sUSER_SID\s*=\s*(({user_sid}[^]]+?))\s*\]""",
  ]
  DupFields = [ "host->dest_host" ]


}
```