#### Parser Content
```Java
{
Name = unix-auditd-kv-user-switch-success-userrolechange
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""audispd""",
"""USER_ROLE_CHANGE""",
""" auid="""
  ]
  Fields = [
"""\s({host}[\w\-.]+)\s+audispd:""",
"""node=({dest_host}[^\s\.]+)""",
"""uid=({user_id}[^\s]+)""",
"""auid=({account_id}[^\s]+)""",
"""pid=({process_id}[^\s]+)""",
"""exe=\"({process_path}[^\"]*)\"""",
"""exe=\"({process_dir}.+\/)({process_name}.+?)\"""",
"""hostname=(({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^\s\.]+))""",
"""addr=({src_ip}[^\s]+)""",
"""res=({result}[^\s'\"]+)"""
  ]
  DupFields = ["dest_host->host"]


}
```