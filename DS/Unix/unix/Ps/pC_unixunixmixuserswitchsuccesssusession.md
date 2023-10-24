#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-susession
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
"""session opened for user""",
"""su:""",
"""(uid="""
  ]
  Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",    
"""\"agent_hostname\":\"(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^\"]+)))\"""",
"""\d\d:\d\d:\d\d (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)))\s+su(:|\[)""",
"""({event_code}su):.+?for user ({dest_user}[^\s]+) by ({user}[\w\.\-]{1,40}\$?)?\(uid=({user_uid}\d+)\)""",
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)? (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)))\s+su(:|\[)""",
"""({event_code}su):.+?for user ({account}[^\s]+) by ({user}[\w\.\-]{1,40}\$?)?\(uid=({user_uid}\d+)\)"""
  ]
  DupFields = ["dest_user->account"]


}
```