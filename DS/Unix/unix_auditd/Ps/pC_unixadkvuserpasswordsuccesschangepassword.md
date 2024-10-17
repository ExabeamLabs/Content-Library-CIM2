#### Parser Content
```Java
{
Name = "unix-ad-kv-user-password-success-changepassword"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
Conditions = [
"""type=USER_CHAUTHTOK"""
"""op=change password"""
"""res=success"""
]
Fields = [
  """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sauid=({account_id}\d+)\s"""
"""\sid=({dest_user_id}\d+)"""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
"""\sid=({dest_user_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```