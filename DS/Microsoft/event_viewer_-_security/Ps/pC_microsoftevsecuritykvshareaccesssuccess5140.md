#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-success-5140"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 5140""", """REMARKS = A network share object was accessed.""" ]
Fields = [
  """({dest_host}({host}[\w\-.]+))\s+ADAuditPlus""",
  """\WTIME_GENERATED\s*=\s*({time}\d{10})""",
  """\WREMARKS\s*=\s*({event_name}[^\]]+?)\s*\]""",
  """\WEVENT_NUMBER\s*=\s*({event_code}\d+)""",
  """\WEVENT_TYPE_TEXT\s*=\s*(null|({result}[^\]]+?))\s*\]""",
  """\WSOURCE\s*=\s*(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[\w\-.]+))""",
  """\WOBJECT_NAME\s*=\s*(?:[\\?]*)(null|({file_path}({object}[^\]]+?)))\s*\]""",
  """\WFILE_NAME\s*=\s*(null|({file_name}[^\\\/]+?(\.({file_ext}[^\.]+?))?))\s*\]""",
  """\WFILE_LOCATION\s*=\s*(?:[\\?]*)(null|({file_dir}[^\]]+?))\s*\]""",
  """\WLOGON_ID\s*=\s*(null|({login_id}[^\]]+?))\s*\]""",
  """\WDOMAIN\s*=\s*(null|({domain}[^\s\]]+?))\s*\]""",
  """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/\"\]]+?)))\s*\]""",
  """\WUSERNAME\s*=\s*(null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\]""",
  """\WRECORD_NUMBER\s*=\s*(null|({event_id}\d+))""",
  """\WUSER_SID\s*=\s*(null|({user_sid}[^\s\]]+))""",
  """\WFORMAT_MESSAGE\s*=\s*(null|({additional_info}.+?))\s*\]""",
  """\WACCESSES\s*=\s*(null|({access}[^\]]+?))\s*\]""",
  """\WUNC_NAME\s*=\s*(?:[\\?*]*)(|null|({share_name}[^\]]+?))\s*\]"""
  """Source Port(=|:)\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```