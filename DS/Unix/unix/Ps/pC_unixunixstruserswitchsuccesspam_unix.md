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
"""\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+(\+|\-)\d\d:\d\d ({host}({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)) ({event_code}\S+)""",
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s+\d{1,2}\s+20\d{2}\s+\d{1,2}:\d{1,2}:\d{1,2})""",
"""\w+\s\d+\s\d\d:\d\d:\d\d\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(;|$|"|\.|\)|\s)""",
"""\"@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\w+\s+\d+ \d\d:\d\d:\d\d(\.\S+)? ({host}({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+))\s+.+?:\s*pam_unix""",
"""session opened for user ({account}.+?) by""",
"""\(uid\\?=({user_id}\d+)\)""",
"""session opened for user \S+ by (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\(""",
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]
  DupFields = [ "host->dest_host", "user_id->user_uid"]


}
```