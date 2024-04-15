#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-move-success-5139"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [ """EVENT_NUMBER = 5139""", """ Account Moved """ ]
Fields = [
  """TIME_GENERATED\s*=\s*({time}\d{10})""",
  """({host}[\w\-.]+) ADAuditPlus""",
  """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
  """({event_name}User Account Moved)""",
  """CALLER_LOGON_ID\s*=\s*({login_id}[^]]+?)\s*\]""",
  """ACCOUNT_DOMAIN\s*=\s*({domain}[^]]+?)\s*\]""",
  """ATTRIBUTES_NEW_VALUE\s*=\s*({new_attribute}[^]]+?)\s*\]""",
  """ATTRIBUTES_OLD_VALUE\s*=\s*({old_attribute}[^]]+?)\s*\]""",
  """\sCORRELATION_ID\s*=\s*(null|({correlation_id}[^]]+?))\s*\]""",
  """ACCOUNT_NAME\s*=\s*(({user}[^]]+?))\s*\]""",
  """ACCOUNT_SID\s*=\s*\%\{(({user_sid}[^]]+?))\}\s*\]""",
  """FORMAT_MESSAGE\s*=\s*(null|-|({ds_object_class}[^\']+?))\s*'"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```