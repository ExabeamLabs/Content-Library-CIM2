#### Parser Content
```Java
{
Name = "unix-ad-kv-group-member-add-success-usermgmt"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = "epoch_sec"
Conditions = [
"""type=USER_MGMT"""
"""op=add-to-shadow-group"""
"""res=success"""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+)\s*(tag_audit_log(:|\s*)|audisp-syslog\[)""",
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sacct="({account_name}[^"]+)""""
"""\sauid="?({account_id}\d+)"""
"""\sgrp="({group_name}[^"]+)""""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```