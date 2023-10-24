#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-passwordexpire
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pam_unix(sshd:account): password for user""", """will expire in""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+sshd""",
    """password for user ({user}[\w\.\-]{1,40}\$?)""",
    """pam_unix\(sshd:account\):\s*({event_name}[^$]*?)\s*$""",
    """({event_code}ssh)""",
  ]
  ParserVersion = "v1.0.0"


}
```