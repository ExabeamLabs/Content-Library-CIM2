#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-authentication-credrefr
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = [ "epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MMM dd HH:mm:ss" ]
  Conditions = [ """CRED_REFR""","""PAM:setcred""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\d\d:\d\d:\d\d ({host}[\w\-.]+)\s*(tag_audit_log(:|\s*)|audisp-syslog\[)""",
    """({time}\d{4}\-\d{1,2}\-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d+)""",
    """({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """msg=audit\(({time}\d{10})""",
    """\saddr=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s""",
    """\sacct="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\sres=({result}[^']+)\'""",
    """\sses=({session_id}\d+)""",
    """exe="({process_path}[^"]*)"""",
    """exe="({process_dir}.*\/)({process_name}[^"]+?)"\s*\w+=""",
    """\sauid=({account_id}\d+)\s""",
    """\suid=({user_id}\d+)""",
    """op=({action}[^\s]+)""",
    """type=({operation_type}\S+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```