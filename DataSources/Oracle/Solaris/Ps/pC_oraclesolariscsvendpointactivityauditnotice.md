#### Parser Content
```Java
{
Name = oracle-solaris-csv-endpoint-activity-auditnotice
  Vendor = Oracle
  Product = Solaris
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """from """,
    """audit.notice""",
    """ID 702911"""
  ]
  Fields = [
    """({time}\d+-\d+-\d+\s\d+:\d+:\d+).[^,]+.[^,]+.({host}[^,]+)""",
    """({event_code}702911)\s({event_name}audit.notice)]\s*({operation}[^\s]+)""",
    """({result}(ok|failed))""",
    """session\s*({login_id}\d+)""",
    """by\s*({user}[^\s]+)""",
    """as\s*({auth}[^\s]+)""",
    """\sin\s({src_zone}[^\s]+)""",
    """from\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """obj\s*(?:({process_path}({process_dir}[^\s]*?)(\/+({process_name}[^\/]+?))?))\s+""",
    """argv\s*({process_command_line}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```