#### Parser Content
```Java
{
Name = unix-unixauditd-kv-user-password-modify-success-grpmgmt
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch_sec"
  Conditions = [ """type=GRP_MGMT""","""op=changing-group-passwd""","""res=success""" ]
  Fields = [
    """msg=audit\(({time}\d{10})\.\d{3}""",
    """\sacct="({account_name}[^"]+)"""",
    """\sses=({session_id}\d+)""",
    """\spid=({process_id}\d+)""",
    """\sgrp="({group_name}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```