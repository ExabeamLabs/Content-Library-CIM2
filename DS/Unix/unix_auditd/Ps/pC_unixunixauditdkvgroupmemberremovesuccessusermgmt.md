#### Parser Content
```Java
{
Name = "unix-unixauditd-kv-group-member-remove-success-usermgmt"
Vendor = "Unix"
Product = "Unix Auditd"
TimeFormat = "epoch_sec"
Conditions = [
"""type=USER_MGMT"""
"""op=delete-user-from-group"""
"""res=success"""
]
Fields = [
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