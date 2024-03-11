#### Parser Content
```Java
{
Name = unix-auditd-kv-user-create-success-addgroup
  Vendor = "Unix"
  Product = "Unix Auditd"
  TimeFormat = "epoch_sec"
  Conditions = [
"""type=ADD_GROUP"""
"""op=add-group"""
"""res=success"""
  ]
  Fields = [
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sacct=\"({account_name}[^\"]+)\""""
"""\sses=({session_id}\d+)"""
"""\spid=({process_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```