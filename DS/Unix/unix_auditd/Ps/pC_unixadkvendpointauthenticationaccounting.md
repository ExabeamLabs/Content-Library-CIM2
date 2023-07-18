#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-authentication-accounting
  Vendor = Unix
  Product = Unix Auditd
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """type=USER_ACCT""","""PAM:accounting""" ]
  Fields = [
    """({host}[\w\-.]+)\s*tag_audit_log:""",
    """msg=audit\(({time}\d{10})""",
    """\saddr=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s""",
    """\sacct="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
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