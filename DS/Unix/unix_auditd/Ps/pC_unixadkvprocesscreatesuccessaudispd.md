#### Parser Content
```Java
{
Name = unix-ad-kv-process-create-success-audispd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""audispd""",
"""USER_CMD""",
""" cmd="""
  ]
  Fields = [
    """node=({host}[^\s\.]+)""",
    """\s({host}[\w\-.]+)\s+audispd:""",
    """\suid=({user_id}[^\s]+)""",
    """auid=({account_id}[^\s]+)""",
    """pid=({process_id}[^\s]+)""",
    """cmd=({process_path}[^\s]+)\s+[\w\=]+""",
    """cmd="?({process_dir}[^"=]*\/)?({process_name}[^"=]+?)\s*("|\(?\w+=|$)""",
    """res=({result}[^\s'"\)]+)"""  
  ]
  DupFields = ["host->src_host"]


}
```