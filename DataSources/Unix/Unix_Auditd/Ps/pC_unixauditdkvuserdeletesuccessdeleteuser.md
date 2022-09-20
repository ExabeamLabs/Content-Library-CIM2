#### Parser Content
```Java
{
Name = unix-auditd-kv-user-delete-success-deleteuser
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch_sec"
  Conditions = [
"""type=DEL_USER""",
"""op=delete-user""",
"""res=success"""
  ]
  Fields = [
"""msg=audit\(({time}\d+)\.\d{3}""",
"""\sauid=({account_id}\d+)\s""",
"""\sid=({dest_user_id}\d+)""",
"""\suid=({user_id}\d+)""",
"""\sses=({session_id}\d+)"""
  ]


}
```