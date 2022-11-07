#### Parser Content
```Java
{
Name = unix-auditd-kv-user-create-success-adduser
  Vendor = "Unix"
  Product = "Unix Auditd"
  TimeFormat = "epoch_sec"
  Conditions = [
"""type=ADD_USER"""
"""op=add-user"""
"""res=success"""
  ]
  Fields = [
"""msg=audit\(({time}\d+)\.\d{3}"""
"""\sauid=({account_id}\d+)\s"""
"""\sid=({account_id}\d+)"""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
"""\spid=({process_id}\d+)"""
  ]
  DupFields = [
"host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```