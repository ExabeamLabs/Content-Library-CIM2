#### Parser Content
```Java
{
Name = unix-auditd-kv-user-switch-success-userrolechange
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["yyyy:MM:dd-HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
""" msg=audit(""",
""" type=USER_ROLE_CHANGE""",
""" auid="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""\s({host}[\w\-.]+)\s+audispd:""",
"""node=({dest_host}[^\s\.]+)""",
"""uid=({user_id}[^\s]+)""",
"""auid=({account_id}[^\s]+)""",
"""pid=({process_id}[^\s]+)""",
"""exe=\"({process_path}[^\"]*)\"""",
"""exe=\"({process_dir}.+\/)({process_name}.+?)\"""",
"""hostname=(({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^\s\.]+))""",
"""addr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""res=({result}[^\s'\"]+)"""
  ]
  DupFields = ["host->dest_host"]


}
```