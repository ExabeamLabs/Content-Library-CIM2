#### Parser Content
```Java
{
Name = unix-ad-kv-process-create-success-audit
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
"""audit""",
"""USER_CMD""",
""" cmd="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d:\d\d:\d\d ({host}[\w\-.]+)\s*(tag_audit_log:|audisp-syslog)""",
    """msg=audit\(({time}\d{10})""",
    """ uid=({user_id}[^\s]+)""",
    """auid=({account_id}[^\s]+)""",
    """pid=({process_id}[^\s]+)""",
    """cmd="?({process_path}[^"]*?)\s*("|\w+=|$)""",
    """res=({result}[^\s'"]+)""",
    """cmd=({process_command_line}[^=]+?)\s*\w+="""
  ]


}
```