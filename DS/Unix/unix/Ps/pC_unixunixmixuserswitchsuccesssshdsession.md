#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-sshdsession
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Conditions = [
"""session opened for user""",
"""(uid=""",
"""sshd:""",
"""_unix"""
  ]
  Fields = [
"""({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)?\s*({host}[\w\-.]+)\ssshd\[""",
"""(::ffff:)?({host}[\w\-.]+)\s+pam_unix""",
"""({time}\d+-\d+-\d+T\d+:\d+:\d+)((\.\d+)?[\+\-]\d+:\d+)""",
"""\(uid=({user_id}\d+)\)""",
"""session opened for user ({account}.+?)(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_id}\d+)\)""",
"""(::ffff:)?({host}[\w.\-]+) sshd ({login_id}\d+) authpriv""",
"""sshd\[({login_id}\d+)""",
"""\d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)\s+""",
"""({event_code}ssh)""",
"""\"host\":\"(::ffff:)?({host}[^\"]+)""",
"""\"timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
"""\d\d:\d\d:\d\d(\.\d+[\-\+\d+:]+)? \[?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+?))\]?\s+sshd\[""",
""""project_id":"({project_id}[^"]+)""""
""""zone":"(-|({zone}[^"]+))""""
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
"""({time}\w\w\w \d\d \d\d:\d\d:\d\d) \[({host}[\w\.\-]+)\]"""
"""({event_name}session opened)"""
  ]
  DupFields = [ "user_id->user_uid", "account->dest_user"]


}
```