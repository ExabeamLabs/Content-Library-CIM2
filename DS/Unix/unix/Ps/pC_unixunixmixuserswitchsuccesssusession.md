#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-susession
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""session opened for user""",
"""su:""",
"""(uid="""
  ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s*su"""
"""({time}\w+\s*\d+\s\d\d:\d\d:\d\d) (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)))\s+su(:|\[)""",
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""", 
"""({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",   
"""\"agent_hostname\":\"(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^\"]+)))\"""",
"""({event_code}su):.+?for user ({dest_user}[^\s]+?)(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_uid}\d+)\))?""",
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)? (::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w.\-]+)))\s+su(:|\[)""",
"""({event_name}session opened for user)"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = ["dest_user->account","user_uid->user_id"]


}
```