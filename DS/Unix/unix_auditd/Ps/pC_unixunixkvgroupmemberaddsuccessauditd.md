#### Parser Content
```Java
{
Name = "unix-unix-kv-group-member-add-success-auditd"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = "epoch_sec"
Conditions = [
"""type=USER_MGMT"""
"""op=add-user-to-group"""
"""res=success"""
]
Fields = [
"""msg=audit\(({time}\d{10})\.\d{3}"""
"""\sacct=\"({account_name}[^\"]+)\""""
"""\sauid=\"?({account_id}\d+)"""
"""\sgrp=\"({group_name}[^\"]+)\""""
"""\suid=({user_id}\d+)"""
"""\sses=({session_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```