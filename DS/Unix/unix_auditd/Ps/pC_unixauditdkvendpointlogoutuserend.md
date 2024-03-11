#### Parser Content
```Java
{
Name = unix-auditd-kv-endpoint-logout-userend
  Vendor = Unix
  Product = Unix Auditd
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """type=USER_END""","""PAM:session_close""" ]
  Fields = [
    """({host}[\w\-.]+)\s*tag_audit_log:""",
    """msg=audit\(({time}\d{10})""",
    """\saddr=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s""",
    """\sacct="({user}[^"]+)"""",
    """\sres=({result}[^']+)\'""",
    """\sses=({session_id}\d+)""",
    """exe="({process_path}[^"]*)"""",
    """exe="({process_dir}.+\/)({process_name}.+?)"""",
    """\sauid=({account_id}\d+)\s""",
    """\suid=({user_id}\d+)""",
    """op=({action}[^\s]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```