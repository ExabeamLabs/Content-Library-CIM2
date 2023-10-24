#### Parser Content
```Java
{
Name = unix-auditd-kv-user-switch-success-sessionopen
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""type=USER_START""",
"""op=PAM:session_open""",
"""res=success"""
  ]
  Fields = [
"""({host}[\w\-.]+)\s*tag_audit_log:""",
"""msg=audit\(({time}\d+)\.\d{3}""",
"""\sacct=\"({account}[^\"]+)\"""",
"""\sauid=\"?({account_id}\d+)""",
"""\suid=({user_id}\d+)""",
"""\sses=({session_id}\d+)""",
"""UID=\"*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
  ]
  DupFields = [ "host->dest_host" ]


}
```