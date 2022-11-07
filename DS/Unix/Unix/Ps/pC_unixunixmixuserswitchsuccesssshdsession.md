#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-sshdsession
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""session opened for user""",
"""(uid=""",
"""sshd:""",
"""_unix"""
  ]
  Fields = [
"""(::ffff:)?({host}[\w\-.]+)\s+pam_unix""",
"""({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)""",
"""session opened for user ({dest_user}.+?) by""",
"""\(uid=({user_id}\d+)\)""",
"""(::ffff:)?({host}[\w.\-]+) sshd ({login_id}\d+) authpriv""",
"""sshd\[({login_id}\d+)""",
"""\d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)\s+""",
"""({event_code}ssh)""",
"""\"host\":\"(::ffff:)?({host}[^\"]+)""",
"""\"timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
"""\d\d:\d\d:\d\d (::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))\s+sshd\[""",
  ]
  DupFields = [ "user_id->user_uid"]


}
```