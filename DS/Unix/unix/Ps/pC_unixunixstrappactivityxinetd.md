#### Parser Content
```Java
{
Name = unix-unix-str-app-activity-xinetd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """xinetd[""",""": ssh""" ]
  Fields = [
  """from=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """pid=({process_id}\d+)\s""",
  """({event_code}ssh)""",
  """({event_name}START)""",
  """({event_name}EXIT)""",
  ]
  ParserVersion = "v1.0.0"


}
```