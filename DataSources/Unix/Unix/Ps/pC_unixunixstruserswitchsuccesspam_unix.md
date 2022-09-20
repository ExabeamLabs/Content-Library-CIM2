#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-success-pam_unix
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""pam_unix(""",
"""session opened for user"""
  ]
  Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\S+)?)\s({host}({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+))""",
"""\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+(\+|\-)\d\d:\d\d ({host}({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)) ({event_code}\S+)""",
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s+\d{1,2}\s+20\d{2}\s+\d{1,2}:\d{1,2}:\d{1,2})""",
"""\w+\s\d+\s\d\d:\d\d:\d\d\s({src_ip}\d+\.\d+\.\d+\.\d+)""",
"""\"@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\w+\s+\d+ \d\d:\d\d:\d\d(\.\S+)? ({host}({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+))\s+.+?:\s*pam_unix""",
"""session opened for user ({dest_user}.+?) by""",
"""\(uid=({user_id}\d+)\)""",
"""session opened for user \S+ by ({user}[^\(\"=,]+)""",
  ]
  DupFields = [ "host->dest_host", "user_id->user_uid"]


}
```