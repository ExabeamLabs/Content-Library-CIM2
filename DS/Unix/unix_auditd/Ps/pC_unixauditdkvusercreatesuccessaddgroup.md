#### Parser Content
```Java
{
Name = unix-auditd-kv-user-create-success-addgroup
  Vendor = "Unix"
  Product = "Unix Auditd"
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
  Conditions = [
"""ADD_GROUP"""
"""op=add-group"""
"""res=success"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sacct=\"({account_name}[^\"]+)\""""
"""\sses=({session_id}\d+)"""
"""\spid=({process_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"
    DupFields = [
"account_name->dest_user"
  ]


}
```