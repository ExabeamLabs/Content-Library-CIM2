#### Parser Content
```Java
{
Name = unix-ad-kv-process-create-success-audit
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""audit""",
"""USER_CMD""",
""" cmd="""
  ]
  Fields = [
    """({host}[\w\-.]+)\s*tag_audit_log:""",
    """msg=audit\(({time}\d{10})""",
    """ uid=({user_id}[^\s]+)""",
    """auid=({account_id}[^\s]+)""",
    """pid=({process_id}[^\s]+)""",
    """cmd="?({process_path}[^"]*?)\s*("|\w+=|$)""",
    """res=({result}[^\s'"]+)"""
  ]


}
```