#### Parser Content
```Java
{
Name = unix-auditd-kv-user-switch-success-sessionopen
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["yyyy:MM:dd-HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
"""type=USER_START""",
"""op=PAM:session_open""",
"""res=success"""
  ]
  Fields = [
  """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""\d\d:\d\d:\d\d ({host}[\w\-.]+)\s*(tag_audit_log(:|\s*)|audisp-syslog\[)""",
"""msg=audit\(({time}\d+)\.\d{3}""",
"""\sacct=\"({account}[^\"]+)\"""",
"""\sauid=\"?({account_id}\d+)""",
"""\suid=({user_id}\d+)""",
"""\sses=({session_id}\d+)""",
"""\W+UID=\"*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\sAUID="""",
  ]
  DupFields = [ "host->dest_host" ,"account->dest_user"]


}
```