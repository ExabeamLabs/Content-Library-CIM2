#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-authentication-creddisp
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """type=CRED_DISP""","""PAM:setcred""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """\d\d:\d\d:\d\d ({host}[\w\-.]+)\s*(tag_audit_log(:|\s*)|audisp-syslog\[)""",
    """msg=audit\(({time}\d{10})""",
    """\saddr=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s""",
    """\sacct="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\sres=({result}[^']+)\'""",
    """\sses=({session_id}\d+)""",
    """exe="({process_name}[^"]*)"""",
    """exe="({process_dir}.*\/)({process_name}[^"]+?)"\s*\w+=""",
    """\sauid=({account_id}\d+)\s""",
    """\suid=({user_uid}\d+)""",
    """op=({action}[^\s]+)""",
    """type=({operation_type}\S+)"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```