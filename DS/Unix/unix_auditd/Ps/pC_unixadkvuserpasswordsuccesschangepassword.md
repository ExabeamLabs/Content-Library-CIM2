#### Parser Content
```Java
{
Name = "unix-ad-kv-user-password-success-changepassword"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = "epoch_sec"
Conditions = [
"""type=USER_CHAUTHTOK"""
"""op=change password"""
"""res=success"""
]
Fields = [
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sauid=({account_id}\d+)\s"""
"""\sid=({dest_user_id}\d+)"""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
"""\sid=({target_user_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```