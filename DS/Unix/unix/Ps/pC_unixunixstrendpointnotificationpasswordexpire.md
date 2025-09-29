#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-passwordexpire
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """pam_unix(sshd:account): password for user""", """will expire in""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+sshd""",
    """password for user ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """pam_unix\(sshd:account\):\s*({event_name}[^$]*?)\s*$""",
    """({event_code}ssh)""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```