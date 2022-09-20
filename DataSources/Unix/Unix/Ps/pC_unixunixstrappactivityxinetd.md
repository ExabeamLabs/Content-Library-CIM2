#### Parser Content
```Java
{
Name = unix-unix-str-app-activity-xinetd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """xinetd[""",""": ssh""" ]
  Fields = [
  """from=(::ffff:)?({src_ip}[A-Fa-f:\d.]+)""",
  """pid=({process_id}\d+)\s""",
  """({event_code}ssh)""",
  """({event_name}START)""",
  """({event_name}EXIT)""",
  ]
  ParserVersion = "v1.0.0"


}
```